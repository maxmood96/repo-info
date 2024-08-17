## `sapmachine:22-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:b032a3893f4106a12c7a03b127567b6bd151452393340c32cae73df190d33d38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:bac6dad1b52184e384f6eed837408fff52317ef4939840abd1deaf29730fe44b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87451080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95ff80288ce5799fde2fb9e8de0580678e9f823c54b172d4ab53ee296b6df4b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46afcbdd85b85904570a2f3f475b49e504c82546e5dc7cd7bb2763539871bae`  
		Last Modified: Sat, 17 Aug 2024 02:02:34 GMT  
		Size: 57.9 MB (57915055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:68572cd9ad5e47de2ee2c68ff3d64d49cbb05e8e4dbf00e434961bf6b9f3f601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2157487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97898d9df2bdc134fbce080fa0712967c032bacab08e320a21b4910afd2cc0b9`

```dockerfile
```

-	Layers:
	-	`sha256:3dfc5f7b6887fb7f078563de401048040f8052d829ca25250bb57f62fe850c5c`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 2.1 MB (2148130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db4f76aa77510de88fb37f0ed50b7b694531184061f067c2c021eeafaa92df08`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 9.4 KB (9357 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:2427188bfe316b64d5ea13ad501e43aca063fa4bc30811719b6a9f1426555dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84271941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0594a949a0c5fc30ced4c29267cecce4d36f8924647c400931bedd46d8507a5d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8066bcdb9d97181a129ee12b600e775b6344278016d192ae0cdf405b24cbf3f8`  
		Last Modified: Sat, 17 Aug 2024 04:10:47 GMT  
		Size: 56.9 MB (56913258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7140d8dd3236c96de3764cafeeb5c47e319295f5c633e9691d30d683eea1cbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2156875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8301e0f76ca4c7d015f5d149ca24b4fc8710e9086f9c1736a7fc72aad7c0ab`

```dockerfile
```

-	Layers:
	-	`sha256:f0c105897098a5b5ce6c7c50dce00332da65587dd54d61633cab747dc1cb5b06`  
		Last Modified: Sat, 17 Aug 2024 04:10:45 GMT  
		Size: 2.1 MB (2147193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:839ec02eef7a08665ce5c1c7f5b642befd4134d7f33eebdb6532eaa0f05159a0`  
		Last Modified: Sat, 17 Aug 2024 04:10:45 GMT  
		Size: 9.7 KB (9682 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5f320d83f10bf868ba26a469999d03bbe824e1b621faa0c221d5bcc0951f048e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93637256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c480c57ab8b56dd752240b3e63087c297ce10171c5626abe0c98c78985699235`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19946e898fd4b25257bc3da3c59d1a687cb013267cb82bf0007cd74b16772bbd`  
		Last Modified: Sat, 17 Aug 2024 02:37:15 GMT  
		Size: 59.2 MB (59173078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5ef299760340a06e9938cfbe2ee5eb8231ed944d0fe14de587ee9ffe0f184150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2160827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc637027274984dcfe1ea27d3ad8b71541725f10d1d2b29ed23524bb07e52ed`

```dockerfile
```

-	Layers:
	-	`sha256:c3e2cdda4b32288e281b3f4a2baf03a40979d0d55c812d80339104aba7436493`  
		Last Modified: Sat, 17 Aug 2024 02:37:13 GMT  
		Size: 2.2 MB (2151420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6a1c473c16c30ee0adbb41c04cbf8eebe05f54db99eb133a9516c7ac43c825d`  
		Last Modified: Sat, 17 Aug 2024 02:37:12 GMT  
		Size: 9.4 KB (9407 bytes)  
		MIME: application/vnd.in-toto+json
