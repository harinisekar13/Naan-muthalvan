# Naan-muthalvan
Introduction

The CRM Application for Jewel Management is a Salesforce-based system designed to automate and streamline jewelry business operations — including inventory tracking, billing, and customer management.
It enables jewelry stores and retailers to manage stock, track sales, update prices, and maintain strong customer relationships within a unified cloud platform.

Developed using Salesforce Developer Edition, this project showcases how Salesforce CRM can be customized for the jewelry industry, integrating custom objects, Flows, Apex triggers, validation rules, and dashboards for a complete, real-time business management solution.

🎯 Objectives

Maintain centralized, real-time customer and inventory data

Automate order processing and billing operations

Enable personalized marketing through customer segmentation

Reduce manual errors using workflows and validation rules

Ensure secure role-based data access

Provide visual insights through dashboards and reports

Optimize sales and customer satisfaction through automation

💡 Ideation

Originality of the Idea

Unlike general CRMs, this system focuses on jewelry industry challenges such as fluctuating gold rates, custom orders, and stock valuation.
It effectively integrates Salesforce capabilities to deliver tailored CRM automation through:

Custom Objects and Relationships

Flows and Process Builder

Apex Trigger and Handler classes

Validation Rules

Role-based Access Control

Reports and Dashboards


Feasibility

Fully achievable using Salesforce Developer Edition (Free)

No third-party tools or licenses needed

Scalable for jewelry retailers, wholesalers, and chains

Supports future AI/ML-based pricing prediction and ERP integration

⚙️ System Design

Custom Objects

1. Jewel_Customer__c – Stores customer information


2. Item__c – Records jewelry details (gold, silver, diamond)


3. Customer_Order__c – Tracks customer orders


4. Price__c – Maintains current gold/silver price and purity data


5. Billing__c – Handles invoices, charges, and total amount



Tabs Created: Jewel Customer, Item, Customer Order, Price, Billing


User Roles

Admin: Full control and configuration access

Sales Executive: Manages customers, leads, and orders

Inventory Manager: Updates product details and stock status

Goldsmith/Worker: Access to assigned records and basic operations


🧩 Features & Automation

Apex Trigger & Handler

Automatically updates the Paid Amount field before record insertion or update in the Billing object.

trigger UpdatePaidAmountTrigger on Billing__c (before insert, before update) {
    if (Trigger.isInsert) {
        UpdatePaidAmountTriggerHandler.handleBeforeInsert(Trigger.new);
    } else if (Trigger.isUpdate) {
        UpdatePaidAmountTriggerHandler.handleBeforeUpdate(Trigger.oldMap, Trigger.new);
    }
}

Flow Automation

Flow Name: Billing Notification Flow
Trigger: On creation or update of Billing record
Action: Sends an automated email to the customer with item and purchase details.

Validation Rule Example

Rule Name: PriceValidationRule
Object: Item__c
Formula:

Price__c <= 0

Error Message: “Item price must be greater than zero.”

📊 Reports & Dashboards

Reports

Sales Report: Shows sales summary per customer and order.

Inventory Report: Displays available stock and valuation.

Billing Summary Report: Summarizes total amount, making charges, and KDM.


Dashboard

JewelryCRM_Dashboard
Includes:

Top-selling products

Monthly sales trend

Low-stock alerts

Revenue breakdown by item type


🧠 Best Use Cases

Jewelry Retail Stores – Track orders, stock, and pricing updates

Wholesalers – Manage bulk sales and supplier performance

Goldsmith Workshops – Monitor item design and return timelines

Multi-branch Chains – Centralized CRM and analytics view


✅ Conclusion

The CRM Application for Jewel Management efficiently automates and integrates jewelry business operations using Salesforce CRM.
It ensures:

Accurate stock management

Faster billing and order processing

Improved customer satisfaction

Data-driven business decisions


The project demonstrates the adaptability of Salesforce to industry-specific needs, making it a robust, scalable, and secure CRM platform for jewelry retailers.

🔮 Future Scope

AI & ML for predicting customer preferences and pricing trends

Mobile App Integration for real-time field sales

ERP Connectivity for full-scale enterprise operations

Blockchain Integration for jewelry authenticity tracking


📚 References

Salesforce Trailhead Modules (Custom Objects, Schema Builder, Validation Rules, Flows, Dashboards)

Project Implementation: Salesforce Developer Edition

Developed by Abinayashree s Harinipriya S Aswathi A Asha K

 🔗 GitHub Repository: https://github.com/harinisekar13/Naan-muthalvan
