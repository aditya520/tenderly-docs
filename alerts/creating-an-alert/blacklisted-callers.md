# Blacklisted Callers

This one is one of the favourite security-oriented alerts: **we can get a notification whenever someone who isn’t whitelisted calls our contract**.

For this example, I’ve set up a simple Gnosis Multisig Wallet which you can [find here](https://dashboard.tenderly.co/contract/kovan/0xbcf55f198e2a5ff4c632610183b1a5290c193e4a?utm_source=medium&utm_campaign=alerting_release&utm_medium=post&utm_content=public_contract_listing).

Now, whenever someone other then the owners of the Multisig Wallet calls this Smart Contract I’ll get an e-mail instantly so that I can react accordingly.

* First things first: add the contract to a Project either via the tenderly push command or using the Verified contract feature. 
* Go to the alerts tab, select the **Whitelisted Callers** rule, and then select the **MultiSigWalletWithDailyLimit** Smart Contract. 
* I’ve added the following addresses to the whitelist \(the owners of the Multisig wallet\): **0xc9E094Deb826b00D10af0aB3D2A62d712e89F67A** and **0xC4dFd227848Fbe6640ab14c9C339845BEd350665.**

Tenderly has a smart delivery algorithm for the e-mails we send your way. You will get notified instantly when something happens, and afterward, you will receive aggregated notifications when it makes more sense, so the spam will be on a bare minimum if any. So you’ll have both the latest alerts from Tenderly and the latest and greats from Netflix at the top of your inbox!
