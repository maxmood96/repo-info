## `sapmachine:25-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:c50a90e7d6178322e12a17f16c3c1f90a2a34cde3199bb0a1729520018c89cfe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:4dc598cb02a8b65a71bfc4a9e56a34854369d21c028d5e89d9644f9cff6cc634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.6 MB (264564708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9505f1c52eecf664e623715231a6d93285958400c36b1c581ac792568aff4146`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753647e261fdd16b9591297f02a82c02b86fba53d72d8ca872423ae41ec496cc`  
		Last Modified: Thu, 02 Oct 2025 14:36:23 GMT  
		Size: 234.8 MB (234841697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b0298e23bfcba5a7b639ad3ba0c66e1a33c391e9c5e20ff64a075768dc8e7a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2359941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb6964535be9ee614bb42df794dc09443bef4650388986b7391f1cee8922c26`

```dockerfile
```

-	Layers:
	-	`sha256:f1268c50ddfb34f0bc14e739a7af4604d3dd0b51517188d293df8db4797e8641`  
		Last Modified: Thu, 02 Oct 2025 09:12:15 GMT  
		Size: 2.3 MB (2348697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03d29556fdf1cb52cf88adc4b6b3be3ac7108081092d7bab257d5a08c227c49c`  
		Last Modified: Thu, 02 Oct 2025 09:12:15 GMT  
		Size: 11.2 KB (11244 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:776b945d20e741c56746d208abe52f931409ce1fb64f1b039df37415b426eb54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261314126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfdd1c677cc2cfbe400918ed5d3987757bdb674c6d2160ead54cee4e6fe0801e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986b01e0be42d0e2e44fd28aff476000f02fa494ca22a3f817356fa0b73fc3f8`  
		Last Modified: Thu, 02 Oct 2025 01:33:21 GMT  
		Size: 232.5 MB (232452551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3dac4c412747127b01389e274aed3e7c2b6935bcec55808c205a7c780e48e484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2360669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c31e2be543b9860d3e1f2dbea9644d53a37dfc2737f6d4f22e9fee70c171312`

```dockerfile
```

-	Layers:
	-	`sha256:b98e71e4f65ba007f3553a88e10b0505aa2c147ac8ed49e6319b8a31b7faa6a3`  
		Last Modified: Thu, 02 Oct 2025 03:10:13 GMT  
		Size: 2.3 MB (2349237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61607fb203c7b1893d610a03ebe3766efbb931c6999cc981a2692771aa11fff8`  
		Last Modified: Thu, 02 Oct 2025 03:10:14 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c75ade5d40f2cf4dc94f0dd867b613633053db9c31b4b6d425e18786d9fb202d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.0 MB (270039961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f72356ef173c79bec19db71e8c53b9664169d880f6718284d3edf5aa1995a8ca`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067484d5b72ea140b59d80c6641cad4eeeee6ad95b803a1bf1e9ade39105b4f4`  
		Last Modified: Thu, 02 Oct 2025 20:39:07 GMT  
		Size: 235.7 MB (235736414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cb4bc2e9c688ca95e8c2e31fdea7aab0778d62de64dd09f5d596ecb7a93b6066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2355481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0618aadbb6769027c7dda64840ed08798523c16538bfb661ff2b0e32dd85f576`

```dockerfile
```

-	Layers:
	-	`sha256:e8f71bf6da8aa6434959efea582a310e68baa12da27c7aaa0692fc88c60972d2`  
		Last Modified: Thu, 02 Oct 2025 06:10:26 GMT  
		Size: 2.3 MB (2344151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a48f6e3eb308bf3ec3d4b98adc86eea45b7175963ed115e5353bacb5933260b`  
		Last Modified: Thu, 02 Oct 2025 06:10:27 GMT  
		Size: 11.3 KB (11330 bytes)  
		MIME: application/vnd.in-toto+json
