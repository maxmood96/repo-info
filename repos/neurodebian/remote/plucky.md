## `neurodebian:plucky`

```console
$ docker pull neurodebian@sha256:94059f498abec3eaeed6dfce79b8e4bb77eaece284f735c2bf5db9bfec213736
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:plucky` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:55a68eac248a8d42afae7771815316c6597bc23414f2bcb24610df9e6dc7e75b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34804798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94188be5c2812cd4d434a3510f2ab091126185cc132c235484f5d8a9ac13d08f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Sep 2025 05:07:41 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:07:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:07:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:07:41 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 10 Sep 2025 05:07:44 GMT
ADD file:1d0db44377aa33c495de438dd435408b4391cf11e887ef1a542a8ab49275c67c in / 
# Wed, 10 Sep 2025 05:07:44 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:47429ff9cdd3006afbf0a7a02f144b5a7444e546614a97a12fd567f7a4e3afdb`  
		Last Modified: Wed, 10 Sep 2025 15:57:53 GMT  
		Size: 28.3 MB (28305856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d950a571b00bde276c30d63f2ee2a5b9567f2fb831c12cd1eb737519ed1480`  
		Last Modified: Tue, 23 Sep 2025 17:39:24 GMT  
		Size: 6.4 MB (6392123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cebe2c7b5214a82ea313c8e78ea11f5ae93f4d1db70d09a1b7265327764c87f9`  
		Last Modified: Tue, 23 Sep 2025 17:39:22 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242a2790fa0f37041a04be6d0aa7128f9deada84df5b813f1d252e0b7b2b5951`  
		Last Modified: Tue, 23 Sep 2025 17:39:22 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b8e683f9c29882925b49af66393f164647dfa8910c654219c5c3e3e4299abd`  
		Last Modified: Tue, 23 Sep 2025 17:39:22 GMT  
		Size: 103.9 KB (103907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:plucky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:81aabe3836e3743663a639189c3c1d1c9c2ff9d04fe9729d8bdd06b7c73aea9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e7dbd796cad8555b51207ba5b6dacc473494b04b36b052b5e21733c861d667`

```dockerfile
```

-	Layers:
	-	`sha256:975dba4328ee4fefd23c6e963d51ed262a6282c5a3c6e80007f4d1aeaba86d5a`  
		Last Modified: Tue, 23 Sep 2025 19:08:33 GMT  
		Size: 2.1 MB (2129591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38214ac78604bf6125c273adcbdfaa727fd4c183ec0ae0ae4d88b3389834d212`  
		Last Modified: Tue, 23 Sep 2025 19:08:33 GMT  
		Size: 14.1 KB (14112 bytes)  
		MIME: application/vnd.in-toto+json
