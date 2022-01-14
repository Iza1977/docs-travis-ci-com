---
title: Writing Probes
layout: en_insights

---

This section helps you to understand what a **"Probe"** is in Travis Insights, how it is structured, and how to edit it yourself.

![Probes_Principal](/user/images-insights/Probes_Principal.png) 

### Probes definition
Each plugin type has a list of predefined probes, you can see the configuration of each one at the moment of setting a probe. Review the [Plugin Types](../plugin-types) section to find a list of predefined probes according to each plugin type.

### Probes functionality
The vast majority of the data which flows through the Travis Insights system is "state" data, this data will tell us about the current state/configuration/status of the infrastructure. Within Travis Insights, this data is all encoded into SREQL. 

### Probes information
At the top of the probes list a drop-down list lets you decide which probes to display, All Probes, Active Probes, or Inactive Probes.

The probes list separates in columns different information:
- **Type**, displays how the probe was created, as a built-in probe (Native Probe) or as a Custom Probe. 
- **Product**, shows the company or community member that contributed/sponsored the probe. The contributor's name is a link to its main informational page. Order the probes alphabetically using the arrow next to the column's name.
- **Category**, indicates the probe category (Infrastructure, Monitoring, Source Control, etc.)
- **Message**, displays de predefined message set in built-in probes or the message you added while creating a custom probe.
- **Tags**, lets you organize probes according to your needs, you can create 10 tags in each probe and add or remove them in the modal view.
- **Status**, shows if it is an Active or Inactive probe.

###  Configure your probes
To add new probes, the **"New Probe"** button displays two options:
- **New built-in probe:** With default information filled up.
- **New custom probe:** With empty fields to configure all data.

In the **Add new Built-in Probe** and **Add new Custom Probe** windows, you will find the following fields:

![addProbe](/user/images-insights/addProbe.png) 

- **Product:** You have a drop-down list with all registered plugins in your Travis Insights account, the category (Infrastructure, Monitoring, Source Control, etc.), and the type (Native, Custom).
- **Probe:** This option is only available for **Built-in Probes** according to the plugin you are adding, you will find a list of predefined probes in each plugin type, for more information visit the [plugin types page](../plugin-types).
- **Notification:** You can set the Notification you want to have according to the selected plugin and probe. In Built-in Probes, this field has predefined information.
- **Description:** The description gives you a better idea of what the Notification is for, you can find here some clues to solve it. In Built-in Probes, this field has already some information.
- **Query:** In this field you can set some SREQL language queries, defining the probe action. In Built-in Probes, this field is already defined according to Plugin and Probe types. To edit and check the functionality you can open the **Probe Editor** by clicking the **EDIT QUERY** button.


> **SREQL Language**
>
> SREQL is a readable and easy scripting language based on SQL syntax that allows you to track state changes and compare them to known/desired configurations.
>
> **Example**
>
>    *SREQL language:*
>
>        SELECT name
>        FROM $.Animals.Dogs
>        WHERE @.Breed = " Rottweiler "
>        ASSERT @.Age > 2
>
>    *Returns:* 
>
>        SELECT name
>        FROM $.Animals.Dogs
>        WHERE @.Breed = " Rottweiler "
>        ASSERT @.Age > 2
>    
> For more information about SREQL visit the <a href="https://docs.srenity.io/docs/sreql-language/">SREQL language</a> page
    
- **Tags:** In this field add tags to identify and order better your probes, you have 20 characters for each tag including spaces and you can add 10 tags maximum per probe. Start writing tag names in the **+Add Tag** space, you can select a tag from the list that displays the ones created before. 

- **Category:** In this section you find two subsections. A field where you can add a **help link** with some relevant information for the probe and the **Weighting Probes** subsection, for more information visit below the Weighting Probes information.


