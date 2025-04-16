## `sapmachine:11-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:0e5bd14f2306e35f243f67c3b4b99e4d87d34aa152e9e05333079d6dd2379f77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:e6e58d383a751e2912175740c9391abecb35f622474419537992e0915a36310c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80104413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b24ebf9daceeda83dc30adbd60faf0c195a52ec9d41f3a871f245aff6a414a5`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:43:12 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:43:14 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 08 Apr 2025 10:43:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:44 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.27 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Apr 2025 10:34:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aeddfc64d0b6733a010fbad8c283c4a62f902bc55c9e2d143988413d95c1539`  
		Last Modified: Wed, 16 Apr 2025 16:14:08 GMT  
		Size: 50.4 MB (50386761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:81c5cc89644df665381c4be10b435291570030bd966bd3f0574b23725c432059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0651cbbac2916c15e58647f894d4c2f3e16c5e1cd864be52d1777501c2c2a2e`

```dockerfile
```

-	Layers:
	-	`sha256:bda716c8f1555a6eff50aaa46462d53cbf866b1944e78fb0b9cf403d762f7361`  
		Last Modified: Wed, 16 Apr 2025 16:14:07 GMT  
		Size: 2.4 MB (2391602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bce7ed2958ecbb5d259c2339e73d1a01cf1f87ebe1484af8432c363b4bb0137d`  
		Last Modified: Wed, 16 Apr 2025 16:14:07 GMT  
		Size: 9.5 KB (9471 bytes)  
		MIME: application/vnd.in-toto+json
