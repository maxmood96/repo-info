## `sapmachine:26-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:ae47968825d5d4a8ed953f6c92d099ce1ff60f4cc98ab94b95c010319585b00f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:26-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:c758eb7fdd1813cdc9406223f86e1668c801f16bb24d858ac6c513e95b6e1f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 MB (254910968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808e4dbe27be88c575d0be54a180c687d22d20c6e67ec5054ca1d8bb20555489`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Wed, 18 Mar 2026 17:48:54 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Mar 2026 17:48:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 18 Mar 2026 17:48:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2a47c7c54e394626a01a9b7fe8da82293f2915363da3afc204b05ebc1c2f22`  
		Last Modified: Wed, 18 Mar 2026 17:49:19 GMT  
		Size: 225.2 MB (225178975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a166e45386be2be53642742ccebf8da9cdedfea11e06e6295dd6be0f9f141598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2356404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70545738568669bbc135c41659b986b7d94a270f07aa75672291ba82b815bca`

```dockerfile
```

-	Layers:
	-	`sha256:47f4a0a1226cd60c68cfb7b755c45f2d30dd570c8c51164b1092bed6d2bbe123`  
		Last Modified: Wed, 18 Mar 2026 17:49:13 GMT  
		Size: 2.3 MB (2346248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81513693702577faeef23988ef5cac0e79fb1cbf07f6cf4a2552ee1e587d97ce`  
		Last Modified: Wed, 18 Mar 2026 17:49:13 GMT  
		Size: 10.2 KB (10156 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:034312cbb801ff37128ff24023c96918cda8a810d2edde16647763af0e9f9664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251908422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97514f11d811b336557590eadb66dab4757be56d1e32c31f535472782697f0e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Wed, 18 Mar 2026 17:48:51 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Mar 2026 17:48:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 18 Mar 2026 17:48:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6830f2a4c50f9a9c94ee0f0bd5e679a7f8e78376a3ffb3106224357842cb5508`  
		Last Modified: Wed, 18 Mar 2026 17:49:15 GMT  
		Size: 223.0 MB (223038713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8c47ef1819524868c1b7d18a55a9dd4a45230673616ccb4a1432256abf5d211a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2357059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf5cb59e27b82c35162f33a46daf7daaf361585fef7599b866e16a4ae1a0a38`

```dockerfile
```

-	Layers:
	-	`sha256:8ab014caf4e3379b1bf8b3a4152213c91f94815f3dc46846be806a1ea363fe4e`  
		Last Modified: Wed, 18 Mar 2026 17:49:11 GMT  
		Size: 2.3 MB (2346752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:482c2a69606ae57c6477073ddc582ded1a6a2ef8802b6dbc7d0c7f04d739a86b`  
		Last Modified: Wed, 18 Mar 2026 17:49:11 GMT  
		Size: 10.3 KB (10307 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:994fc80cd8f415e41c372ef6f3612f50cf333c744bf0afcc6f5ed9d7deeca2c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.5 MB (260543621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296bf08985e24fa1e85e8fd879fea3faa61dda80969b7628edae4753ccbea28d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 17:18:33 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:18:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:18:36 GMT
ADD file:2a89eb67bf550d9680999e3ff99dbaa17c251b6c343a241318e879a26da53fca in / 
# Mon, 23 Feb 2026 17:18:37 GMT
CMD ["/bin/bash"]
# Wed, 18 Mar 2026 17:46:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Mar 2026 17:46:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 18 Mar 2026 17:46:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf53574e46790fcd623e0f19bebd50667f50fcfd4f3d30424bd481c740c9e7f`  
		Last Modified: Wed, 18 Mar 2026 17:47:35 GMT  
		Size: 226.2 MB (226233570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:15a67a3a3e7c4c666b0603c7d4efe57c9e19e03db46689948a0f48af49c04149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2353326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36f8512f96c2786e29e8f6ea35953d82bcd4652da07b75373aa0537f928e40d`

```dockerfile
```

-	Layers:
	-	`sha256:4f96dc71b5f4bf34b5a0eca4ad67694c96ceb54c57681d43a3a337d861888549`  
		Last Modified: Wed, 18 Mar 2026 17:47:31 GMT  
		Size: 2.3 MB (2343101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efdde2fe03c8f5f387ac5e70ea5b5eff4da714d7d04a53526f6054174db51b37`  
		Last Modified: Wed, 18 Mar 2026 17:47:31 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json
