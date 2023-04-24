## `archlinux:base`

```console
$ docker pull archlinux@sha256:f88544eecbe2b463e8e74c68241ef7ce0a5340fa93395abc05d4083036ece9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:595a8241225577ea4b5f59525a90162a605dae30a9ab9407a458e6464a644cc9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143087297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131484c87d34b86f8fee051730fc272af52cdf601088db8bfcdeafb25471ca04`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 24 Apr 2023 19:20:10 GMT
COPY dir:711e487feaff3aace3eed1534ac4c28ec247530f292c0e5fa7e5e5a7c9b30714 in / 
# Mon, 24 Apr 2023 19:20:12 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 24 Apr 2023 19:20:12 GMT
ENV LANG=C.UTF-8
# Mon, 24 Apr 2023 19:20:12 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:0b6e80fc7ef7ba341bd8106e1a07e9d326554fc5d43f17a5b12231f517f2b692`  
		Last Modified: Mon, 24 Apr 2023 19:22:01 GMT  
		Size: 143.1 MB (143079342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be24523ca07449101615d90f4b4ebb99892f0ba2296b98cca8c2b086ca5ae0d7`  
		Last Modified: Mon, 24 Apr 2023 19:21:41 GMT  
		Size: 8.0 KB (7955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
