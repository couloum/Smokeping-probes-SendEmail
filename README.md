Smokeping-probes-SendEmail
==========================

Smokeping probe that mesure time needed to send an email

AUTHORS
=======

Florian Coulmier <florian@coulmier.fr>

INSTALL
=======

Copy file SendEmail.pm into the probes directory of smokeping
(/usr/local/smokeping/lib/Smokeping/Probes)

Add the following configuration in the 'Probes' section of your smokeping 
config file
(/usr/local/smokeping/etc/config)

--------------------------------------------------
+ SendEmail
from = your_mail_from@your_domain.com
to = your_rcpt_to@your_domain.com
subject = "Test Smokeping"
--------------------------------------------------

Then, add a target that use this probe in your config file, in the 'Targets'
section.

--------------------------------------------------
++ MySmtpServer
probe = SendEmail
host = mymxhost
--------------------------------------------------

Restart Smokeping and watch the new graphs!

REQUIREMENTS
============

This probe only require Net::SMTP module that should be shipped with your
default perl installation

COPYRIGHT
=========

Copyright (c) 2012 Florian Coulmier <florian@coulmier.fr>

LICENSE
=======

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
