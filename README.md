buleprint
=========

Tool for collect system configuration

1. This tool can collect system information including files(only can get from /etc and /usr/local/), packages, services, source code.
2. It's depends on Git, it will create local git repository.
3. Create module for puppet and chief.

some test:

1. Using two servers(test1, test2)
2. Install extra software which is nginx on test1, test2 is empty
3. Using blueprint on test1, it will store in the local git repository (.blueprints.git)
4. Using blueprint to export the information to a shell code, then copy to test2
5. Running the shell code on test2. test2 will same as test1, auto install the nginx.

Result:

1. The information only can be collected via yum, gem, perl/pecl, etc. 
2. Just can clone the file in /etc(for service and system) and /usr/local(for source code and app). this is not convenient for us.
3. If we are using puppet or chief, maybe we can think about to use blueprint, it's good support to these two software.
