# Dynatrace-License-Ansible

An [Ansible](http://www.ansible.com) role for automated deployments of a [Dynatrace](http://bit.ly/dttrial) license. 

**Note**: Currently, we support only Linux hosts, support for installing Windows hosts is in the making.

## Download

The role is available via:

- [Ansible Galaxy](https://galaxy.ansible.com/list#/roles/2626)
- [GitHub](https://github.com/Dynatrace/Dynatrace-License-Ansible)

## Requirements

Place your license as ```dtlicense.key``` in the role's ```files``` directory from where it will be picked up during the automated installation.

You can obtain a free trial license for Dynatrace from [bit.ly/dttrial](http://bit.ly/dttrial).

## Role Variables

As defined in ```defaults/main.yml```:

| Name                                            | Default               | Description |
|-------------------------------------------------|-----------------------|-------------|
| *dynatrace_license_linux_dynatrace_install_dir* | /opt/dynatrace        | The directory that contains an installation of the Dynatrace Server. |
| *dynatrace_license_linux_license_owner*         | dynatrace             | The file owner of the license file after deployment. |
| *dynatrace_license_linux_license_grou*p         | dynatrace             | The file group of the license file after deployment. |
| *dynatrace_license_file_name*                   | dynatrace-license.dtf | The file name of the Dynatrace License in the role's ```files``` directory. |
| *dynatrace_license_role_name*                   | Dynatrace-License     | The actual name of this role in an [Ansible Playbook's](http://docs.ansible.com/playbooks.html) ```roles``` directory. |

## Example Playbook

	- hosts: all
	  roles:
	    - { role: Dynatrace-License }

## Additional Resources

- [Slide Deck: Automated Deployments](http://slideshare.net/MartinEtmajer/automated-deployments-slide-share)
- [Slide Deck: Introduction to Automated Deployments with Ansible](http://www.slideshare.net/MartinEtmajer/introduction-to-automated-deployments-with-ansible)

## Questions?

Feel free to post your questions on the Dynatrace Community's [Continuous Delivery Forum](https://community.dynatrace.com/community/pages/viewpage.action?pageId=46628921).

## License

Licensed under the MIT License. See the LICENSE file for details.
