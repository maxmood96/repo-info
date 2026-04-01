## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:a6f405f7ce0df315e79e2816670d94a410acab25933e5a44570e827fe4abada8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:684f89bb320fc15f269d733cfc19ed0b5c1f15f199d940085a3c02b90d82831a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33276221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebb4f514f1106446659c0c35b5cc154c33519bede72d75513eeea1e81f3011f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:43:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:43:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Mar 2026 01:43:12 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 17 Mar 2026 01:43:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2863a40c7a7170ba503ee516d26f3a9b818e2606f0ab87535ae76ac0536c121`  
		Last Modified: Tue, 17 Mar 2026 01:43:24 GMT  
		Size: 3.6 MB (3624431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547e46402d925046cbc9b8dda38ed4b4ec4ca3f6d1ff4f41bdcad1a51b430df5`  
		Last Modified: Tue, 17 Mar 2026 01:43:24 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186cd36fecf717d7daa1ec85dd00593dabc4d1aaca1422a24f4c94f4be810c1b`  
		Last Modified: Tue, 17 Mar 2026 01:43:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b72342ac61240026a61da0af1991417b699c7c5b770c54de65b56cc8fc5094a`  
		Last Modified: Tue, 17 Mar 2026 01:43:24 GMT  
		Size: 111.1 KB (111090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:050a384cc4ff3ef04511d6bc797ace854cec23734e8230395615d68d79fd7665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74fde8449d2e512592b6d172bd38f04836912e06bd08a3e7e4d5797564753d14`

```dockerfile
```

-	Layers:
	-	`sha256:8ad6a29f65124fca407209fed2dffb3670b2dafb4eac073c87b2e3a537485f8d`  
		Last Modified: Tue, 17 Mar 2026 01:43:24 GMT  
		Size: 2.2 MB (2198320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c407f459a18d56ccb69cbe43ea0e204e87401d236be87a31ef1e52b5672d30a5`  
		Last Modified: Tue, 17 Mar 2026 01:43:24 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:56de5ce50bc6484dfad202db32b89a2f2ca4d48557aa48e4cf11d390d6da73bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31325059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913e7ec62ad9077f24a0b24e72ecc4fa55fc5e7b77ce11f79f53bf152cb8eec1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:14:35 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:14:36 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 Apr 2026 20:14:36 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 01 Apr 2026 20:14:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f628ca3d20e1c17214b7d1cfb648c745e7ea7a5fc3188f05a7a757a2de998d`  
		Last Modified: Wed, 01 Apr 2026 20:14:51 GMT  
		Size: 3.6 MB (3604788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80793066cb18af083cfac67a17a06c1e4afd12ea6ace3fa8f6f8a613d469756`  
		Last Modified: Wed, 01 Apr 2026 20:14:51 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2368eee4161f30a527478029668d0d63de762edb4a59fba3555fa62c09279eed`  
		Last Modified: Wed, 01 Apr 2026 20:14:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3674a38a9279ec2d8a0bb18ed63f4e177a930c5e9be7229b354701d6769b50`  
		Last Modified: Wed, 01 Apr 2026 20:14:51 GMT  
		Size: 111.2 KB (111153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:12e4211b6e6d2c9a0ea2b79782e147901a46b2ee80063c345077a1ec63b5cd55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8c580742abfd21791b0d471b0ce3169207288db6a9055b3b11eba03a1a593f`

```dockerfile
```

-	Layers:
	-	`sha256:391329d2b648bdb436cd1b6af1bdfc3a3143bfb69f62a4fb083a16013a6ae01e`  
		Last Modified: Wed, 01 Apr 2026 20:14:51 GMT  
		Size: 2.2 MB (2198580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31201397be8aef44a004153ad48cb4a0c7c73f929badb242256dcd2610935155`  
		Last Modified: Wed, 01 Apr 2026 20:14:51 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json
