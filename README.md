# Dynatrace-License-Ansible

An [Ansible](http://www.ansible.com) role for automated deployments of a [Dynatrace](http://bit.ly/dttrial) License. 

## Download

The role is available via:

- [Ansible Galaxy](https://galaxy.ansible.com/list#/roles/2626)
- [GitHub](https://github.com/Dynatrace/Dynatrace-License-Ansible)

## Requirements

Place the Dynatrace License as ```dynatrace-license.key``` in the role's ```files``` directory from where it will be picked up during the automated installation. Alternatively, you can make the Dynatrace License available at an HTTP, HTTPS or FTP resource and point the installation script to the right location, see below. **You can obtain a free trial license for Dynatrace from [bit.ly/dttrial](http://bit.ly/dttrial).**

## Role Variables

As defined in ```defaults/main.yml```:

| Name                                            | Default                                          | Description |
|-------------------------------------------------|--------------------------------------------------|-------------|
| *dynatrace_license_linux_dynatrace_install_dir* | /opt/dynatrace                                   | The directory that contains an installation of the Dynatrace Server. |
| *dynatrace_license_linux_license_owner*         | dynatrace                                        | The file owner of the license file after deployment. |
| *dynatrace_license_linux_license_grou*p         | dynatrace                                        | The file group of the license file after deployment. |
| *dynatrace_license_file_name*                   | dynatrace-license.key                            | The file name of the Dynatrace License in the role's ```files``` directory. |
| *dynatrace_license_file_url*                    | http://localhost/dynatrace/dynatrace-license.key | A HTTP, HTTPS or FTP URL to the Dynatrace License in the form (http\|https\|ftp)://[user[:pass]]@host.domain[:port]/path. |
| *dynatrace_license_role_name*                   | dynatrace.Dynatrace-License                      | The actual name of this role in an [Ansible Playbook's](http://docs.ansible.com/playbooks.html) ```roles``` directory. |

## Example Playbook

	- hosts: all
	  roles:
	    - role: dynatrace.Dynatrace-License

## Testing

We use [Test Kitchen](http://kitchen.ci) to automatically test our automated deployments with [Serverspec](http://serverspec.org):

1) Install Kitchen and its dependencies from within the project's directory:

```
gem install bundler
bundle install
```

2) Run tests

```
kitchen test
```

## Additional Resources

- [Blog: How to Automate Enterprise Application Monitoring with Ansible](http://apmblog.dynatrace.com/2015/03/04/how-to-automate-enterprise-application-monitoring-with-ansible/)
- [Blog: How to Automate Enterprise Application Monitoring with Ansible - Part II](http://apmblog.dynatrace.com/2015/04/23/how-to-automate-enterprise-application-monitoring-with-ansible-part-ii/)
- [Slide Deck: Automated Deployments](http://slideshare.net/MartinEtmajer/automated-deployments-slide-share)
- [Slide Deck: Automated Deployments (of Dynatrace) with Ansible](http://www.slideshare.net/MartinEtmajer/automated-deployments-with-ansible)
- [Slide Deck: Testing Ansible Roles with Test Kitchen, Serverspec and RSpec](http://www.slideshare.net/MartinEtmajer/testing-ansible-roles-with-test-kitchen-serverspec-and-rspec-48185017)
- [Tutorials: Automated Deployments (of Dynatrace) with Ansible](https://community.compuwareapm.com/community/display/LEARN/Tutorials+on+Automated+Deployments#TutorialsonAutomatedDeployments-ansible)

## Questions?

Feel free to post your questions on the Dynatrace Community's [Continuous Delivery Forum](https://community.dynatrace.com/community/pages/viewpage.action?pageId=46628921).

## License

Licensed under the MIT License. See the LICENSE file for details.
[![analytics](https://www.google-analytics.com/collect?v=1&t=pageview&_s=1&dl=https%3A%2F%2Fgithub.com%2FdynaTrace&dp=%2FDynatrace-License-Ansible&dt=Dynatrace-License-Ansible&_u=Dynatrace~&cid=github.com%2FdynaTrace&tid=UA-54510554-5&aip=1)]()
