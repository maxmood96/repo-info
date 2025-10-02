## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:601a9326e0a01d824205506822eb0d0b09a022e87c0383dbdec7ae4fefc52094
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:6e7f58bb0cfe1bea3aad771ecabd3a44351dc0a9f5932dabf7ec4519ad107f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33392869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921c74d53c91f9ad2210028b2a0641105d5aa867dc06219db16d00d87ad81ad4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccbf205b0feed79e5a4c0fd567b19ca963dbf78a57d11fc40829d8c4e97332a`  
		Last Modified: Tue, 23 Sep 2025 19:50:17 GMT  
		Size: 3.6 MB (3562782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72cb51ace634b4c46be5cfb2b382a2ff2593246498d7f91b23878bc384da4994`  
		Last Modified: Tue, 23 Sep 2025 19:50:17 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e752d4601b9ad24a79f82c0d2e65a331623203915426246c09b29b10d1daff`  
		Last Modified: Tue, 23 Sep 2025 19:50:17 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fed9e79b1808f3bfb39d86ef7054ee5aaddfbbc29138f02a9e27be064290626`  
		Last Modified: Tue, 23 Sep 2025 19:50:17 GMT  
		Size: 103.7 KB (103728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c0601720cf5237977e729e625168c37135934a5bfad7c6d11bd16caa3abfb2bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0bdfba6fb54c95cd9b03ea726d2d73347752552939d7511d32863543fd93df`

```dockerfile
```

-	Layers:
	-	`sha256:778594aca3ad20875cc6e85e9bd7a41cbca87b1aad2dd7b1cd395e8343555f42`  
		Last Modified: Tue, 23 Sep 2025 22:08:16 GMT  
		Size: 2.1 MB (2120865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c646c57bd302244cf50328462ef336139f1b76f7ef0b61c85c8b191c2578a22`  
		Last Modified: Tue, 23 Sep 2025 22:08:17 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:076ee02e994b28c4a5b8dca7ce94c0f397d53bf29584490bd1aa926ed68f3fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32530114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:967aac5c12962e1d96fe8450ccb5368757669504e3dd34bbd125834fcee87385`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5d958d3bf78161fb8399d840252a91e567621f23d8189ec65cf293daeb29e9`  
		Last Modified: Thu, 02 Oct 2025 01:27:26 GMT  
		Size: 3.6 MB (3561059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed06b06cf1782d19fce6854a3fdbd239671d3c0de2b7950030170d34daa68a8`  
		Last Modified: Thu, 02 Oct 2025 01:27:26 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae680b1104d31c61ce1e3fe7a96e662af254480a8959d2cbc333210779552d77`  
		Last Modified: Thu, 02 Oct 2025 01:27:26 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b997e8e2c8ba403851c3d5a909927a6b9fd30e7a663418e0bf508fc166bd59e`  
		Last Modified: Thu, 02 Oct 2025 01:27:26 GMT  
		Size: 104.6 KB (104569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:57dd191d5f7c286cf74f6038e19a321e4fbbe2cdef34cc598341f17fd604f5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92002c627339bfe8e554b57adb9a10dae839783d84629f5a0b88d875a93c524`

```dockerfile
```

-	Layers:
	-	`sha256:9080f7f8187a0300ca15ea60cb19daf274f8b2affc20fd54f7c5a0046bf05db3`  
		Last Modified: Thu, 02 Oct 2025 04:07:49 GMT  
		Size: 2.1 MB (2121910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:158d749cd930e4e3a30c6b24908775a1b0162badfc7aae6623b1779e5fdb00a7`  
		Last Modified: Thu, 02 Oct 2025 04:07:50 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json
