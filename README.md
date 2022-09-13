# unbork_ohai_rpm_plugin

Dirty fix for a bug in the OHAI RPM plugin which is triggered by cookbook based OHAI plugins.

When an OHAI plugin exists in a cookbook, it triggers a reload of OHAI, but the
RPM plugin unconditionally redefines a couple of constants causeing an error.

This cookbook patches the RPM plugin until a new version is released for CC17

Has been minimally tested on Ubuntu, but not yet on Windows.
