# HashiCrop `packer` Template of NGiNX
This repo contains a `packer` template for building a Vagrant Base Box of [Ubuntu 16](http://releases.ubuntu.com) (aka xenial-xerus) which includes a [NGiNX](https://nginx.org/en/) http server.


## Usage
```bash
packer build ubuntu16-nginx.json ;
# ...
# ... SUCCESSFUL GENERATION SHOULD RESULT IN:
# ... nginx64.box

vagrant box add --name nginx nginx64.box ; # register box
vagrant init nginx ; # on success a Vagrantfile is generated
vagrant up ;
vagrant ssh ; # ssh to running instance
# ...
# ...
# ...
vagrant destroy -f ... ; # when done to remove.
vagrant box remove -f ... --provider virtualbox ; # to remove local images.
```

See [vagrantup.com/aphorise/boxes/ubuntu16-nginx](https://app.vagrantup.com/aphorise/boxes/ubuntu16-nginx) for generated image.

## Notes
This is intended as a mere practise / training excercise - make proper adjustments & reviews where intending to extend toward full pledged usage.


## Related:
See original template extended for this use case 
 * [aphorise/hashicorp.packer-ubuntu16-xenial-xerus](https://github.com/aphorise/hashicorp.packer-ubuntu16-xenial-xerus)
------
