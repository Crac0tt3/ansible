# ansible
---
- name: Maintenance on TSE
  hosts: all

#  vars_prompt:
#    - name: "Message"
#      prompt: "Entrez votre message"
#      private: no
#      default: "localhost"

  vars:
      Message: A que coucou

  tasks:
  - name: Ping TSE
    win_ping: 

  - name: send msg
    win_shell: msg.exe /server:192.168.138.134 * "{{ Message }}"
