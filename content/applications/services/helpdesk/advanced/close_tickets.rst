===============
Closing Tickets
===============

Once work has been completed on a :guilabel:`Helpdesk` ticket, there are several ways it can be
closed. Manually closing solved tickets keeps the pipeline up to date, while automatically closing
inactive tickets prevents unnecessary blocking issues. Allowing customers to close their own tickets
minimizes confusion around whether an issue is considered solved or not. This results in increased
operational capacity for support teams, and higher customer satisfaction.

Manually closing solved tickets
===============================

As work on a ticket progresses, it is moved along to the next stage in the pipeline. Once the issue
is solved, the ticket is moved to a *folded* stage, to signify the work has been completed. This
marks the ticket as *closed*.

To fold a stage, navigate to the :guilabel:`Helpdesk` dashboard and click on a team to open the
pipeline. Choose a stage, and click on the gear icon at the top right of that stage's kanban column.

.. image:: close_tickets/closing-edit-stage-gear.png
   :align: center
   :alt: View of stage on Helpdesk pipeline with emphasis on gear icon and edit stage option.

.. warning::
   Clicking the gear icon also displays the option to :guilabel:`Fold` the stage. This setting folds
   the stage **temporarily** to simplify the kanban view. This does **not** close the tickets in
   this stage. It also does not permanently fold the stage. If a stage needs to be folded so the
   tickets can be marked as closed, continue following the steps below.

Select :guilabel:`Edit Stage`. This will open the stage's settings page. Check the box labeled
:guilabel:`Folded in Kanban`. :guilabel:`Save & Close`.

   .. image:: close_tickets/closing-folded-setting.png
      :align: center
      :alt: Stage settings page.

Automatically closing inactive tickets
======================================

Tickets that are inactive for a set period of time can be automatically closed. At that point,
they will be moved to a folded stage.

Go to the team's settings page by going to :menuselection:`Helpdesk --> Configuration --> Teams`.
Under the :guilabel:`Self-Service` section, enable :guilabel:`Automatic Closing`.

If one of the team's stages is set to be folded in the kanban view, it will be the default selection
in the :guilabel:`Move to Stage` field. If the team has more than one folded stage, the stage that
occurs first in the pipeline will be the default. If no stage is folded, the default selection will
be the last stage in the pipeline.

The :guilabel:`After days of inactivity` field defaults to `7`, but can be adjusted if necessary.

.. warning::
   The :guilabel:`After days of inactivity` field does **not** take the working calendar into
   account when tracking the amount of time a ticket has been inactive.

If only certain stages should be used to track days of inactivity, they can be added to the
:guilabel:`In Stages` field.

.. example::
   A team's pipeline is created with the following stages:

   - `New`
   - `In Progress`
   - `Customer Feedback`
   - `Closed`

   Tickets can linger in the `Customer Feedback` stage, because once an issue is solved, customers
   may not respond immediately. At that point, they can be closed automatically. However, tickets in
   the `New` and `In Progress` stages may remain inactive due to assignment or workload issues.
   Closing them automatically may result in issues going unsolved.

   Therefore, the :guilabel:`Automatic Closing` settings would be configured as below\:\

   .. image:: close_tickets/closing-automatic-settings-example.png
      :align: center
      :alt: Example Automatic Closing settings.

Allowing customers to close tickets
===================================

Enabling the :guilabel:`Closure by Customers` setting allows customers to close their own tickets
when they determine their issue is resolved.

Start by navigating to :menuselection:`Helpdesk --> Configuration --> Teams` and select
a team. On the team's settings page, scroll to the :guilabel:`Self-Service` section and check the
box for :guilabel:`Closure by Customers`.

.. image:: close_tickets/closing-by-customer-setting.png
   :align: center
   :alt: Customer closing setting in Odoo Helpdesk.

Once the ticket closing settings are enabled, a :guilabel:`Close Ticket` button will be available
for customers when they view their ticket.

.. image:: close_tickets/closing-customer-view.png
   :align: center
   :alt: Customer view of ticket closing in Odoo Helpdesk.

.. note::
   Customers are able to view their tickets by either logging into the portal (if they have access),
   or by clicking the :guilabel:`View the ticket` link they receive by email. The link is included
   in the :guilabel:`Request Acknowledgment` template, which is added to the first stage of a team
   by default.
