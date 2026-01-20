## `sapmachine:lts-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:047d358519a79381708cc4866209d4678b3db5a46e91421fa87693132df592ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:e2614a6997771c8d240206664f953f06a971655d5d2880c999912bfcf89cdeec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248356448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2f4c947cbc0b4a3b6d89a02bce82590c89181d518b3f01c008128a3d9e62dc`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:42:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:42:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 15 Jan 2026 22:42:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952b4095861abb4ffc9d7727a7a406cb460a4d7dbc2683358aaa622c0c764312`  
		Last Modified: Thu, 15 Jan 2026 22:43:33 GMT  
		Size: 218.8 MB (218819781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9bb20030ee1aa1f884ede93c00cf45da854e5a493002e22d8bbfdc3b7f91b2d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2378779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:088c57b58e3d100d9e670e59e35176057e23ac7618c9c3579ced9b32fa7cd4e7`

```dockerfile
```

-	Layers:
	-	`sha256:2f0db4514bdfe30f33f91882cf8dccf2fd00ce83057d1f0f782ca79c73b63e43`  
		Last Modified: Thu, 15 Jan 2026 22:42:47 GMT  
		Size: 2.4 MB (2368506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:804130501b8305839733e452819343f690d397d0c4999c4950b0383ad4c928df`  
		Last Modified: Fri, 16 Jan 2026 01:14:59 GMT  
		Size: 10.3 KB (10273 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:874f27dfce7e013b101f35f40938a5b3a857b0c267b6790fd44c66939c966b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243911180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c90cb49d9417426b84a08f98ca4b752c8653752f0ba33a314141311f7d940a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:45:40 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:45:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 15 Jan 2026 22:45:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321f3fe102a2016224a230c78074329bc72d0ed1f474689010f6fc61c3f4acf5`  
		Last Modified: Thu, 15 Jan 2026 22:46:16 GMT  
		Size: 216.5 MB (216527683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e19e27f4eba0d6e8281f0b3b64edc644a62ae2944f6f16070028278061bdf94d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2378648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011eb40b6d5a5b4eb7daf9fc414d036dbe2941f66a2c2b430796360857724576`

```dockerfile
```

-	Layers:
	-	`sha256:7106787edacef11491ce82bf6ec2740f312f1b5e40ff8f79510dd18bcfefcd65`  
		Last Modified: Fri, 16 Jan 2026 01:15:04 GMT  
		Size: 2.4 MB (2368223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:354a2db2a4a333526bd0a57df0bd642b8fc9a162d0d2e2c19695d03dbcf1cc5d`  
		Last Modified: Fri, 16 Jan 2026 01:15:04 GMT  
		Size: 10.4 KB (10425 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a9530a4ec3f542f36c61575ac0a81f011c896a73a8d9074985be0cac0cc8d0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253811179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75980698d07564f7c9942a4e28682c7deab3db0c14d7398c173f4dd3e4938352`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:04 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:08 GMT
ADD file:db1efb6f83d2e5fbbebd44054afcb57c6ffff071d50a2434a5322064fe97af59 in / 
# Fri, 09 Jan 2026 07:03:08 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 23:30:00 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:30:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 15 Jan 2026 23:30:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Thu, 15 Jan 2026 21:43:22 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0620ed93fbdff2d0b636f18a21a6d39b366eb8d330ff2f36636b0b9900df52`  
		Last Modified: Thu, 15 Jan 2026 23:31:45 GMT  
		Size: 219.4 MB (219364217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:857ffe72c6618d90847ba4749c84c9da09699680ec3e5d32890fe4dcd3464e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2374331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f21b55d5c4aeda0a1c984e4ad568348dbefbccac40166149c58065b2e6aa33`

```dockerfile
```

-	Layers:
	-	`sha256:4e06e25e34bbff97fe724d887a3ea53156f65a22856c3458997c6027f677e82a`  
		Last Modified: Fri, 16 Jan 2026 01:15:09 GMT  
		Size: 2.4 MB (2363991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f66ded07524a2c7cbce4220700bf79e0972fd77d8e1b797fed5ffb654551e84`  
		Last Modified: Fri, 16 Jan 2026 01:15:10 GMT  
		Size: 10.3 KB (10340 bytes)  
		MIME: application/vnd.in-toto+json
