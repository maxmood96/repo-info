## `sapmachine:lts-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:5395d8b96827fb816951cf7136f351f5d8a083fd6bfbed726a062c03d8659f6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:fc68fcaa67d676650e2bcf8f5a37e4449a57d253e2a3a8f433c0f7403eaeb467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251186621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e566a075b42bd644aabbbcbcd4a3813a95e40bbddfb080dd67c0a9f39369a20`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:32:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:32:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 07 Apr 2026 02:32:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26b10bfa4727ab845dfc17be8eff800ac074681c0592ebf25fee26916dc79fa`  
		Last Modified: Tue, 07 Apr 2026 02:33:03 GMT  
		Size: 221.5 MB (221453162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0fef9bacb197fc6fd36d9b70979cca76d8c2ea05b38f3f31b0b4a13dfd039c89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2613669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e8eb336e34e076a71fd1e626d54a29f52caa52637839ae68cfd0c2bf76f03b`

```dockerfile
```

-	Layers:
	-	`sha256:0b2ed7f98dd30b830f5e73c35a39d3d5d76e722564c04113e45dcfbd95cdff87`  
		Last Modified: Tue, 07 Apr 2026 02:32:59 GMT  
		Size: 2.6 MB (2598827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdc842470355690e8e633e5651adf04b1c0a785d1fe62a88a656dcba1684b96d`  
		Last Modified: Tue, 07 Apr 2026 02:32:59 GMT  
		Size: 14.8 KB (14842 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:8fe4e030028decc09407ce462b1dd0e2133b87d3120d5a3d5b66017fd58183da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.1 MB (248140656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2ad37c16806149e45b926073b54cf09ae127c8bfe9ab86df0872448d52751b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:38:50 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:38:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 07 Apr 2026 02:38:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071039733a9216930b6563942a42f349dfb95ab664b4c80b6dc59d7fdf8bb476`  
		Last Modified: Tue, 07 Apr 2026 02:39:14 GMT  
		Size: 219.3 MB (219266581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:37d9e4df63b05c199851169bf154d954efc1568ab62fc796bdcc21a647f59347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2614694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8eedcaf9fe78c8f3f550e2fd0f0a641d7bfac9dab75213844a78c43c31c6c7`

```dockerfile
```

-	Layers:
	-	`sha256:24b1bb4edd9fdf4ec8b7a8f29b21ab06921ef189a67388d34909cb209a023f4e`  
		Last Modified: Tue, 07 Apr 2026 02:39:09 GMT  
		Size: 2.6 MB (2599520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3a7f3f01642af376b8dcd44f90b928f7422b42205a3f50898efd243126d1711`  
		Last Modified: Tue, 07 Apr 2026 02:39:09 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1095bc492b5edbb897421e0dd7469393cfee96b4b9346c1c4122249829531b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256665007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f7645ab8c1196291eae52d9b53ac2987deff50cb4c1f9e44e1ab50860adeb7`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 09:02:49 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:02:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 07 Apr 2026 09:02:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af1eb519a9c0294d2c0ffba67fd5006cf829710f4a208f1d662a7e0118dfaf9`  
		Last Modified: Tue, 07 Apr 2026 09:03:35 GMT  
		Size: 222.4 MB (222351673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c0102d4d9ec3ed1586dc82b8e0db4882a9ede5e221ad5e9e1145dc1d781ed7b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2610851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94adf693b63798ecf63141e633136ec6f31deeaf3bdc96ba2c8ca2992921411d`

```dockerfile
```

-	Layers:
	-	`sha256:49edb7e283e35097fac399c6e443afb31e083a9c5b744fe10ad13c85d5a363e6`  
		Last Modified: Tue, 07 Apr 2026 09:03:30 GMT  
		Size: 2.6 MB (2595851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:042beccf89ba4ddc07b4d87181969a853c17a53caf55a659d6ae1162b9f373e8`  
		Last Modified: Tue, 07 Apr 2026 09:03:29 GMT  
		Size: 15.0 KB (15000 bytes)  
		MIME: application/vnd.in-toto+json
