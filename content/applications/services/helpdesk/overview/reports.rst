=========
Reporting
=========

Odoo's :guilabel:`Helpdesk` app includes several reports that provide the opportunity to track
trends for customer support tickets, identify areas for improvement, manage employee workloads,
and confirm when customer expectations are met.

Available reports
=================

The following are the reports available in Odoo :guilabel:`Helpdesk`. To view the different reports,
go to :menuselection:`Helpdesk --> Reporting`.

Ticket Analysis
---------------

The :guilabel:`Ticket Analysis` report provides an overview of every customer support ticket in the
database, including the number of tickets assigned among teams and individual users. This report is
useful in identifying where teams are spending the most time, and determining if there is an uneven
workload distribution among the support staff.

The default report counts the number of tickets per team and groups them by stage.

.. image:: reports/reports-tickets-default.png
   :align: center
   :alt: View of Ticket Analysis report default view

Alternative measures can be selected to track where the most time is spent at different points in
the workflow. To change the measures used in the report, click :guilabel:`Measures` and choose from
the drop-down menu. The available measures for the :guilabel:`Ticket Analysis` report include:

- Average Hours to Respond
- Hours Open
- Hours Spent
- Hours to Assign
- Hours to Close
- Hours to First Response
- Hours to SLA Deadline
- Rating /5
- Count

SLA Status Analysis
-------------------

The :guilabel:`SLA Status Analysis` report tracks how quickly an :abbr:`SLA (Service Level
Agreement` is fulfilled, as well as the success rate of individual policies. By default, the report
is filtered to show the number of :abbr:`SLAs (Service Level Agreements)` failed, as well as the
failure rate over the last 30 days, grouped by team.

.. image:: reports/reports-sla-status.png
   :align: center
   :alt: View of Group by options of Ticket Analysis report

To change the measures used in the report, click :guilabel:`Measures` and choose from the drop-down
menu. The available measures for the :guilabel:`SLA Status Analysis` report include:

- % of Failed SLA
- % of SLA in Progress
- % of Successful SLA
- Number of SLA Failed
- Number of SLA Successful
- Number of SLA in Progress
- Working Hours to Assign
- Working Hours to Close
- Working to Reach SLA
- Count

.. example::
   To see the number of tickets that were able to achieve the stated :abbr:`SLA (Service Level
   Agreement)` objectives, and track the amount of time it took to achieve those objectives, click
   :menuselection:`Measures --> Number of SLA Successful` and :menuselection:`Measures --> Workings
   Hours to Reach SLA`. To sort these results by the team members assigned to the tickets, select
   :menuselection:`Total --> Assigned to`.

.. seealso::
   - :doc:`sla`

Customer Ratings
----------------

The :guilabel:`Customer Ratings` report displays an overview of the ratings received on individual
support tickets, as well as any additional comments submitted with the rating.

.. image:: reports/reports-customer-ratings.png
   :align: center
   :alt: View of the kanban display in the Customer Ratings report

Click on an individual rating to see additional details about the rating assigned by the customer,
including a link to the original ticket.

.. image:: reports/reports-ratings-details.png
   :align: center
   :alt: View of the details of an individual customer rating

.. tip::
   Select :guilabel:`Visible Internally Only` to hide a rating from the customer portal.

The :guilabel:`Customer Ratings` report is displayed in a kanban view by default, but can also be
displayed in graph or pivot view.

.. seealso::
   - :doc:`ratings`

Choosing the view and filters
=============================

The best view to display a report will depend on the what data is being measured, and how it needs
to be grouped. See below for additional information on the available views for the
:guilabel:`Helpdesk` reports.

.. note::
   Only one measure may be selected at a time for graphs, while pivot tables can include multiple
   measures.

Using the pivot view
--------------------

The *pivot* view presents data in an interactive manner. All three :guilabel:`Helpdesk` reports are
available in the pivot view.

Switch a report to the pivot view by selecting the icon at the top right of the screen.

.. image:: reports/reports-pivot-view.png
   :align: center
   :alt: View of the SLA status analysis report in Odoo Helpdesk

To add a group to a row or column, click the plus button (:guilabel:`+`) next to :guilabel:`Total`,
and then select one of the groups. To remove one, click the minus button (:guilabel:`-`) and
de-select.

Using the graph view
--------------------

The *graph* view presents data in either a *bar*, *line*, or *pie* chart. Switch to the graph view
by selecting the icon at the top right of the screen. To switch between the different chart views,
select the appropriate icon at the top left of the chart.

.. tabs::

   .. tab:: Bar chart

       .. image:: reports/reports-bar-chart.png
          :align: center
          :alt: View of the SLA status analysis report in bar view

   .. tab:: Line chart

       .. image:: reports/reports-line-chart.png
          :align: center
          :alt: View of the Customer Ratings report in line view

   .. tab:: Pie chart

       .. image:: reports/reports-pie-chart.png
          :align: center
          :alt: View of the Ticket analysis report in pie chart view

.. tip::
   Both the :guilabel:`Bar Chart` and :guilabel:`Line Chart` can be viewed :guilabel:`Stacked`.
   This presents two or more groups to appear on top of each other instead of next to each other,
   making it easier to compare data.

Save and share a favorite search
--------------------------------

The :guilabel:`Favorites` feature allows users to save their most commonly used filters without
having to reconstruct them every time they are needed.

To create and save new :guilabel:`Favorites`:

- Set the necessary parameters using the :guilabel:`Filters`, :guilabel:`Group By` and
  :guilabel:`Measures`.
- Click :menuselection:`Favorites --> Save current search`.
- Rename the search.
- Select :guilabel:`Use by default` to have these filter settings automatically displayed when
  the report is opened. Otherwise, leave it blank.
- Select :guilabel:`Share with all users` to make this filter available to all other database
  users. If this box is not checked, it will only be available to the user who creates it.
- Click :guilabel:`Save`.

.. image:: reports/reports-save-filters.png
   :align: center
   :alt: View of the save favorites option in Odoo Helpdesk

.. seealso::
   - :doc:`receiving_tickets`
   - :doc:`Odoo Reporting </applications/general/reporting>`
