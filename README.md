# DebianActions
Acciones a realizar en un debian despues de instalar

# Cambiar los predictable names de los interfaces (Volver a eth0...)

editar /etc/default/grub

en la linea GRUB_CMDLINE_LINUX 

cambiar  a

  GRUB_CMDLINE_LINUX="net.ifnames=0 biosdevname=0"

luego actualizar el grub: 

grub-mkconfig -o /boot/grub/grub.cfg

Antes de rearrancar el Pc IMPORTANTE, cambiar los nombres de Interfaz en 
/etc/network/interfaces 

y ya que te pones, si quieres, configura la IP fija

auto eth0
iface eth0 inet static
        address 192.168.1.244
        netmask 255.255.255.0
        network 192.168.1.0
        broadcast 192.168.1.255
        gateway 192.168.1.1

