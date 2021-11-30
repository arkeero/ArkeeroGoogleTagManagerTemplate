# Arkeeo Pixel

An advertiser can set up the Arkeero conversion pixel using GTM, to keep track the session ID is required to use our arktrid parameter in landing url

- http://advertiser-landing.com/?arktrid=123456789123456

If you use any ad server, the advertiser should do an extra configuration on it to always keep the arktrid parameter.

## Installation Page View

Firstable it must be installed a Page View pixel. This setup seeks arktrid param on URL and keep as a cookie.

![](https://drive.google.com/file/d/19q4UntSMMLYYdusBcxqpNL723K-3gAPj/view?export=view)

Must fire when on landing Page View event

![](https://drive.google.com/file/d/1QeID6VFPmZ0b2-aNvbRGkgXWnvmEz787/view?usp=sharing)

## Register Lead

This tag is the last one to fire and execute a request to Arkeero transaction pixel, adding site Transaction ID.

To register leads, the transaction pixel must be configured. Receive three optional parameters.

- Offer ID: This is an optional value, must be shared by your account manager.
- Transaction ID: This is Transaction Id by landing page, must share in this field. If your landing doesn't return a transaction ID could be send a unique value, hashed email, phone number, etc.hashed email, phone number, etc.
- Revenue: If you want to track revenues, you must share in this field.

![](https://drive.google.com/file/d/1E81ARTYFp18dd4rhkxWvcEe-BP_nF7BX/view?usp=sharing)

Is necessary that this tag is the last one to fire and have do at the moment the transaction happen. It's common that this happens on the Thank you page but can be in other moment (event lead or Send form.). Be careful of where this is set up, as if it fires earlier or later it can be an issue because we won't count the correct transactions.

Make sure to set a tag sequence from Advanced Settings and then Tag Sequencing.
- Select the "Fire a setup tag before Arkeero Lead fires".
- Select the set_arktrid tag from the menu.

![](https://drive.google.com/file/d/1sI15NPEd1kemVF5TROXJSPH19sueW5-s/view?usp=sharing)

## Goal Lead
This one is used to tag each step of the funnel or can count a special event on the Landing Page.

This tag receives three optional parameters and one required param.

- Goal ID: This value has been shared by your account manager; each one should be unique by goal.
- Offer ID: This is an optional value, must be shared by your account manager.
- Transaction ID: This is Transaction Id by landing page, must share in this field. If your landing doesn't return a transaction ID could be send a unique value, hashed email, phone number, etc.
- Revenue: If you want to track revenues, you must share in this field.

![](https://drive.google.com/file/d/1hXy00W7f3jmLVsnNlb1woZJTh1vC5Cd-/view?usp=sharing)

Is necessary that this tag must fire when the transaction happen. It's common that this happens on event, click or another step in the funnel. Be careful of where this is set up, as if it fires earlier or later it can be an issue because we won't count the correct transactions.

Make sure to set a tag sequence from Advanced Settings and then Tag Sequencing.
- Select the "Fire a setup tag before Arkeero Lead fires".
- Select the set_arktrid tag from the menu.

![](https://drive.google.com/file/d/1sI15NPEd1kemVF5TROXJSPH19sueW5-s/view?usp=sharing)
