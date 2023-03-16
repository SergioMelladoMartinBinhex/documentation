=========================
Create a second warehouse
=========================

A *warehouse* is a physical building or space where items are stored. In Odoo, it is possible to set
up multiple warehouses and transfer stored items between them.

By default, the Odoo platform has one warehouse that is already configured, with the address set as
the company's address. To create a second warehouse, select :menuselection:`Configuration -->
Warehouses --> Create` and configure the form as follows:

- :guilabel:`Warehouse`: the full name of the warehouse
- :guilabel:`Short Name`: the abbreviated code by which the warehouse is referred to; the short name
  for the default warehouse in Odoo is "WH"
- :guilabel:`Company`: the company that owns the warehouse; this can be set as the user's company or
  as the company of a customer or vendor
- :guilabel:`Address`: the address where the warehouse is located

.. important::
  The options below will only appear if the :guilabel:`Multi-Step Routes` checkbox is enabled in
  :menuselection:`Configuration --> Settings` under the *Warehouse* heading.

- :guilabel:`Incoming/Outgoing Shipments`: select the routes that incoming and outgoing shipments
  should follow
- :guilabel:`Resupply Subcontractors`: allow subcontractors to be resupplied from this warehouse
- :guilabel:`Manufacture to Resupply`: allow for items to be manufactured in this warehouse
- :guilabel:`Manufacture`: select the route that should be followed when manufacturing goods inside
  the warehouse
- :guilabel:`Buy to Resupply`: check the box to allow for purchased products to be delivered to the
  warehouse
- :guilabel:`Resupply From`: select warehouses that can be used to resupply the warehouse being
  created

.. image:: create_a_second_warehouse/new_warehouse_configuration.png
  :align: center
  :alt: A filled out form for creating a new warehouse.

.. important::
  Creating a second warehouse will automatically enable the *Storage Locations* setting, which
  allows location tracking of products within a warehouse. To toggle this setting, navigate to
  :menuselection:`Configuration --> Settings` and click the checkbox under the *Warehouse* heading.

After filling out the form, click :guilabel:`Save` and the new warehouse will be created.

Add inventory to a new warehouse
================================

If a new warehouse is created that has existing inventory, this should be added to Odoo so that
overall product counts are accurate. To add inventory to a new warehouse, start from
:guilabel:`Inventory` and select :menuselection:`Operations --> Inventory Adjustments --> Create`,
then fill out the inventory adjustment form as follows:

- :guilabel:`Inventory Reference`: the name or code that the inventory adjustment can be referred to
  by
- :guilabel:`Locations`: the location or locations where the inventory is stored; include the new
  warehouse and any locations within it that inventory will be added to
- :guilabel:`Products`: include all products that will be added to inventory or leave blank to
  select any product during the next step
- :guilabel:`Include Exhausted Products`: include products with a quantity of zero; does not affect
  inventory adjustments for new warehouses since they have no existing inventory
- :guilabel:`Accounting Date`: the date used by accounting teams for bookkeeping related to the
  inventory
- :guilabel:`Company`: the company that owns the inventory; can be set as the user's company or as a
  customer or vendor
- :guilabel:`Counted Quantities`: choose whether the counted quantities for products being added
  should default to stock on hand or zero; does not affect inventory adjustments for new warehouses
  since they have no existing inventory

.. image:: create_a_second_warehouse/inventory_adjustment_configuration.png
  :align: center
  :alt: A filled out form for an inventory adjustment.

Once the form is properly configured, click on :guilabel:`Start Inventory` to be taken to the next
page where products can be added to the inventory adjustment. Add a new product by clicking on
:guilabel:`Create` and then fill out the product line as follows:

- :guilabel:`Product`: the product being added to inventory
- :guilabel:`Location`: the location where the product is stored; this can be the new warehouse or a
  location within the warehouse
- :guilabel:`Lot/Serial Number`: the lot that the product belongs to or the serial number used to
  identify it
- :guilabel:`On Hand`: the total number of the product stored in the location for which inventory is
  being adjusted; this should be zero for a new location or warehouse
- :guilabel:`Counted`: the amount of the product that is being added to inventory
- :guilabel:`Difference`: the difference between the *On Hand* and *Counted* values; this will
  automatically update to reflect the value entered in the :guilabel:`Counted` column
- :guilabel:`UoM`: the unit of measure used for counting the product

.. image:: create_a_second_warehouse/product_line_configuration.png
  :align: center
  :alt: Include a line for each product being added to inventory.

After adding all the products already stored in the new warehouse, click
:guilabel:`Validate Inventory` to complete the inventory adjustment. The values in the
:guilabel:`On Hand` column will update to reflect those in the :guilabel:`Counted` column and the
products added will appear in the inventory of the new warehouse.
