Here we are going to give authorization to the users.

Policies are nothing but a means to give authorization to user, who can do what.

To write policies:

Step 1: Click hamburger icon and select identity and security
Step 2: Click Policies tab and create policy.
Step 3: In statements add below policies:

Allow group 'development-domain'/'oci-admin-group' to manage all-resources in compartment development

Allow group 'development-domain'/'oci-admin-group' to manage users in compartment development

Allow group 'development-domain'/'oci-admin-group' to manage domains in compartment development

Allow group 'development-domain'/'oci-admin-group' to manage groups in compartment development

Allow group 'development-domain'/'oci-admin-group' to manage dynamic-groups in compartment development

Allow group 'development-domain'/'oci-admin-group' to manage policies in compartment development

Allow group 'development-domain'/'oci-admin-group' to manage compartments in compartment development


These are some required policies one need to give to admin to do day to day tasks.
