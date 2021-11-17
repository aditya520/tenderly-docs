# Intro to Web3 Actions

**Tenderly Web3 Actions** will run your code in response to on-chain (or even off-chain) events, usually on your smart contracts.&#x20;

You can use Web3 Actions to create custom scenarios in order to further deepen your debugging process, create alerting patterns that are not available out-of-the-box in the [**Alerting**](../alerts/creating-an-alert/) section, automating testing or live production execution in the [**Simulator**](../simulations-and-forks/how-to-simulate-a-transaction/) and [**Forks**](../simulations-and-forks/how-to-create-a-fork/), or anything else that comes to (your) mind.

The code Web3 Actions run is called a _**function**_. The function must be written in TypeScript (or JavaScript) and run in Node 14 runtime. Specification of events that your action listens to is called a _**trigger**_. There are 4 types of triggers:

* **Transaction** - runs a function in response to transactions, with statuses like _as soon as the transaction is mined_ or _after 10 blocks have passed_ and filters such as _emitted events,_ _invoked methods_, etc.
* **Block** - runs your function when the block is mined on a chosen chain(s).
* **Webhook** - runs your function when a request is POSTed to an endpoint.
* **Periodic** - runs your function in periodic intervals or configured CRON.

### Getting Started

To get started,  run `tenderly actions init` in a directory where you want to initialize actions project, which will lead you through setting up a project for your Web3 Actions.

{% hint style="warning" %}
You will need [**Tenderly CLI**](https://github.com/Tenderly/tenderly-cli)** **to initialize Web3 Actions. You will need [**npm**](https://www.npmjs.com) if you are using TypeScript actions or use `tenderly actions init --language javascript.`
{% endhint %}

After initialization, the project contains:

* `tenderly.yaml` with the specification of all actions (e.g. name, description, etc.) and their triggers. For more details, see the [**configuration**](configuration.md) page.
* `actions` directory (or whatever is chosen during setup) where functions implementation should go including files `package.json` or `tsconfig.json` in the case of TypeScript.

{% hint style="warning" %}
All `tenderly actions` commands must be run from a directory that contains `tenderly.yaml.`
{% endhint %}

When you initialize actions project, you must select a Tenderly project which will be used for deploying your actions. You can deploy actions from multiple locations to the same Tenderly project. You can also initialize actions multiple times in the same directory and select a different Tenderly project for each initialization.&#x20;

{% hint style="info" %}
If your actions are very different or have different dependencies, it is recommended to separate them. You can still you same Tenderly project to deploy them.
{% endhint %}

If your actions have dependencies, `node_modules` directory located in the same directory with your actions source files will be packaged and deployed with your actions. `npm install` must be run from a directory where actions sources are. Note that this might be a different directory than one where you run `tenderly actions` commands.&#x20;

{% hint style="warning" %}
Zipped dependencies must not exceed 45MB. Reach o
{% endhint %}

### Deploying Actions

To view your actions in the dashboard, you must deploy them first. Run `tenderly actions deploy` in an initialized project to deploy generated example and go to provided link to view the action in the dashboard. If you initialized actions for multiple projects in the same directory, you will be asked to select a project which you want to deploy. All actions for a single project are deployed together.

{% hint style="info" %}
Deployed action can be stopped through the dashboard. Action will stay deployed, but it won't run automatically.
{% endhint %}

If you just want to validate configuration or build implementation without deploying it, run `tenderly actions build`.

### Manual Trigger

While action must specify trigger type, it doesn't have to configure a trigger. Without a configured trigger, the action will never run automatically. But you can still run your action manually! This can be useful for testing. Navigate to the specific action and click the **Manual Trigger** button.

You can provide any payload you want, as long as it matches the required schema. If your trigger type is transaction or block, you can fetch a transaction or block from a network instead of manually creating a payload.

If you deployed initialized block action, here is an example of a valid payload:

```json
{
  "network": "1",
  "blockNumber": 1000,
  "blockHash": "0x5b4590a9905fa1c9cc273f32e6dc63b4c512f0ee14edc6fa41c26b416a7b5d58"
}
```

{% hint style="success" %}
You can use a manual trigger even if the action is stopped.
{% endhint %}

Next, we are going to describe how to write a function and what runtime features are available.