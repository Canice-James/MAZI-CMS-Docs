# Payment systems

This document provides information on how to add a new payment system to the Content Management System (CMS).

## Create a payment system

This section outlines the standard process for manually adding a new payment system from scratch.

1. Select a project in the CMS and navigate to the **Payment systems** tab in the left-side menu.
2. Check for duplicates to ensure the payment system you plan to add does not already exist.
3. Click the **Add new** button.

![Payment systems page](open_payment_systems_tab.png)

<a id="step_4"></a>
4. In the open **Add paySystem dialog**, fill in the form, paying special attention to key parameters and configuration sets required to set up the payment system: *Name*, *Icon Code*, *Countries to Implement*, and *Deposit*.

![Add paySystem dialog](add_paySystem_dialog.png)

* **Alias**: Descriptive label or identifier for the payment system. It can be generated automatically based on the “Name” and “Deposit” values.
* **Name**: Payment system name.
* **Provider Code**: Parameter applicable to cryptocurrency payment systems.
* **Icon Code**: Payment system icon code.
* **Hide Amount**: Parameter applicable to certain payment systems.
* **Trusted** and **Trusted Count**: Parameters used for payment systems that support both trusted and non-trusted transaction flows.
* **Countries to Implement**: Countries where the payment system is operational.
* **Allowed Deposit Systems for Withdrawal**: Payment systems whose deposits qualify for withdrawals through other permitted payment systems. For example, if you specify “iq_creditcard” here, funds deposited via this payment system will be eligible for withdrawal through another payment system designated for withdrawals, such as "iq_bankintl".

![Deposit configuration set](deposit_configuration_set.png)

* **Deposit**: Deposit rules and particularities to be defined as a configuration set.
  * **Currency**: Available currencies; each new currency has to be added separately.
  * **Payment System**: Payment system name.
  * **Preset Value**: One or more predefined payment amounts to be shown to customers for quick selection.
  * **Min Value**: Minimum amount a customer can deposit in a single transaction.
  * **Max Value**: Maximum amount a customer can deposit in a single transaction.
  * **Default Value**: Amount to be selected by default.
  * **Fee**: Applicable transaction fee (e.g., "0%").
  * **Processing Time**: Estimated time for processing transactions (e.g., "Instant").
* **Withdrawal**: Withdrawal rules and particularities to be populated manually or copied from the “Deposit” configuration (see the preceding figure).

![Other configuration parameters](follow_up_configuration_parameters.png)

* **Scenario**, **Scenario for Deposits**, and **Scenario for Withdrawals**: Parameters applicable to certain online casinos (brands).
* **Additional Field**: One or more parameters applicable to payment systems that operate directly rather than through DevCode, e.g., “iq_xxx”.
* **Comments**: Additional notes. Keep in mind that this and other content might need translation into supported languages.

5. Select the newly added payment system in the table on the **Payment systems** page and then click “R”, “P”, or both above this table to specify the environment where this payment system will be available: Release, Production, or both.

![Environments](release_prod_environments.png)

6. Deploy the payment system to the selected environment. Upon completion, you will see the corresponding environment indicators (“R”, “P”, or both) in the **Show** column.

## Copy a payment system

This section explains how to create a payment system by duplicating an existing one.

1. Select a project in the CMS and navigate to the **Payment systems** tab in the left-side menu.
2. Find the payment system you want to use as a template in the table and then select it.
3. Click the **Copy to project** button above the table.

![Copy a payment system to a project](copy_ps_to_project.png)

4. In the open **Copy to projects** dialog, select the target project where you want to add the new payment system, select the **Force** check box, and then click the **Apply** button.

![Add a payment system to a project](add_ps_to_project.png)

5. Click to modify the copied payment system in the **Edit paySystem** dialog. (Refer to [step 4](#step_4) from the previous section for details on each parameter.)

![Edit paySystem dialog](edit_paySystem_dialog.png)

6. Specify the environment where this payment system will be available (“R” for Release, “P” for Production, or both) and then deploy it. (Refer to steps 5 and 6 from the previous section for more information.)

## Establish trusted and non-trusted flows

A payment system can be configured to manage risk and security by ensuring that higher-risk transactions undergo additional verification steps or follow different processing routes. This setup is controlled by the”Trusted” and “Trusted Count” parameters.

To implement trusted and non-trusted flows, you need to create two associated payment system configurations—either from scratch or by duplicating an existing one:

* One for trusted transactions (“Trusted” = “trusted”).
* One for non-trusted transactions (“Trusted” = “non-trusted”).

These configurations are mutually exclusive with regular payment systems that do not distinguish trusted and non-trusted flows (“Trusted” = “common”). Therefore, if you implement a trusted/non-trusted setup, any existing common flow configuration should be removed.

In this section, you will go through the process of establishing trusted and non-trusted flows, considering the following example:

* Transactions initiated by customers who have made up to three deposits are deemed riskier and routed through a provider with stricter security measures: “iq_creditcard(ecommpay)”.
* Transactions initiated by more trustworthy customers are deemed reliable and processed by a more optimized provider: “iq_creditcard(securetrading)”.

---

1. Select a project in the CMS and navigate to the **Payment systems** tab in the left-side menu.
2. Create two associated payment systems—either from scratch or by duplicating existing ones—one for the trusted flow (“iq_creditcurd(securetrading)”) and the other for the untrusted flow (“iq_creditcard(ecommpay)”), specifying the “Trusted” and “Trusted Count” parameters accordingly. (Refer to [step 4](#step_4) from the "Create a payment system" section for details.)

![Trusted in Edit paySystem dialog](edit_paySystem_trusted.png)

3. Specify the environment where these payment systems will be available (“R” for Release, “P” for “Production” , or both) and then deploy them. (Refer to steps 5 and 6 from the “Create a payment system” section for more information.)
4. Check for existing payment systems with “Trusted” = “common” and remove them if detected.

![Check common payment systems](check_common_ps.png)
