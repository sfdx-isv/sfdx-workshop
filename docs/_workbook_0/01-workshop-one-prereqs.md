---
title: "Prerequisites for Workshop One: Building Managed Packages with SFDX"
permalink: /prerequisites/workshop-one/
excerpt: "Excerpt TBA"
last_modified_at: 2019-05-29
toc: false
classes: wide
---

## Step One: Install the Salesforce CLI

**Why?** The Salesforce CLI is at the heart of Salesforce DX.  Almost everything we do will involve the CLI in one way or another.
{: .notice--success}

* Visit [https://developer.salesforce.com/docs/atlas.en-us.sfdx_setup.meta/sfdx_setup/sfdx_setup_install_cli.htm](https://developer.salesforce.com/docs/atlas.en-us.sfdx_setup.meta/sfdx_setup/sfdx_setup_install_cli.htm)
* Follow the instructions that are specific to your Operating System (macOS, Windows, or Linux)
* Make sure you read and follow the instructions for **“Verify Your Installation”** (second to last section on the page) to ensure that you've correctly installed the CLI

## Step Two: Install Visual Studio Code

**Why?**  Visual Studio Code (VS Code) is the official IDE for Salesforce development (ie. no more Eclipse).  Almost all of the exercises will use VS Code in one way or another.
{: .notice--success}

* Visit [https://code.visualstudio.com/Download](https://code.visualstudio.com/Download)
* Download the installer for your Operating System
* Run the installer once it's downloaded to your machine

## Step Three: Install the Salesforce Extensions for VS Code

**Why?** VS Code is the IDE, but the Salesforce Extensions for VS Code actually let you talk to the Salesforce CLI.  Luckily, installing plugins with VS Code is a breeze.
{: .notice--success}

* Visit [https://developer.salesforce.com/tools/extension_vscode](https://developer.salesforce.com/tools/extension_vscode)
* Follow all of the steps listed under “Getting Started”

## Step Four: Make sure the Developer Hub Feature is Enabled in Your PBO

**Why?** Dev Hubs inside of Partner Business Orgs (PBOs) have special entitlements that other DevHubs don't get. While you _can_ complete Workshop One with a DevHub from a trial or DE org, you _should_ use the DevHub in your PBO, if possible.
{: .notice--success}

* Login to your PBO (Partner Business Org)
    * **NOTE:** If you do not have access to your company's PBO, you can use a __new__ trial or DE org as your Dev Hub instead of your PBO. If you go this route, remember that you'll be limited to 3/6 active/daily scratch orgs. 
* Open Setup and type “Dev Hub” in the Quick Find search box
    * **IMPORTANT:** If you _do not_ have the Dev Hub feature available in Setup, please use the following troubleshooting steps
        * Make sure the org you're in is _really_ your PBO and not a random org that you _think_ is your PBO
        * Open a case with support and ask them to activate the Dev Hub in your PBO and provide you with the appropriate entitlements (exact entitlements will depend on your partner status)
* Click on the **Dev Hub** setup item
* If it's not already enabled, flip the switch to enable the Dev Hub

## Step Five: Make Sure That Your Dev Hub Org has “My Domain” Setup

**Why?**  One of the key features of Salesforce DX for ISVs is the linking of a packaging org's namespace to your Developer Hub in order to create “namespaced scratch orgs”.  To make this work, your Dev Hub org _must_ have My Domain enabled _and_ deployed to users.
{: .notice--success}

* If not already configured, setup My Domain for your Dev Hub (PBO) org by following these instructions: [Define your MyDomain Subdomain Name](https://help.salesforce.com/articleView?id=domain_name_define.htm)
* If you are setting up My Domain now, you must deploy it to users after turning it on.  You can do that by following these instructions:  [Test and Deploy Your New My Domain Subdomain](https://help.salesforce.com/articleView?id=domain_name_testing_and_rollout.htm&type=0)

## Step Six: Create a _NEW_ Developer Edition Org

**Why?** This DE (Developer Edition) org will be used during the workshop to build a simple managed package.  Creating it ahead of time will let us move quickly through the exercises during the workshop.
{: .notice--success}

**IMPORTANT:** Please make sure you create a _NEW_ DE org so you can start with an empty managed package. Please _do not_ try to use a previously existing DE or Packaging org.

* Use your Environment Hub to create a Partner Developer Edition (PDE) or standard Developer Edition (DE) org.
    * If you're having any issues with your Environment Hub, you can also go to [https://developer.salesforce.com/signup](https://developer.salesforce.com/signup) to get a standard DE org 
    * **IMPORTANT:** You _must_ create a Developer Edition org (either PDE or DE) because you'll be using it later to create a managed package
* Register a Namespace Prefix for your DE org by following the instructions on this page: [https://developer.salesforce.com/docs/atlas.en-us.packagingGuide.meta/packagingGuide/register_namespace_prefix.htm](https://developer.salesforce.com/docs/atlas.en-us.packagingGuide.meta/packagingGuide/register_namespace_prefix.htm)
* Create an _empty_ managed package named “My Managed Package” by following Step #1. Create a Package about halfway down this page:  [https://developer.salesforce.com/docs/atlas.en-us.packagingGuide.meta/packagingGuide/packaging_uploading.htm](https://developer.salesforce.com/docs/atlas.en-us.packagingGuide.meta/packagingGuide/packaging_uploading.htm)
    * **IMPORTANT:** Do not add any components to your package and do not upload a package version. We'll do that together during the workshop.

