## `sapmachine:25-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:38193ad3259affe52f1a8ddb0e959a76330ff9639728d072a65e0b4cbb143801
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
$ docker pull sapmachine@sha256:89b25c7b2b3b58592fba5ed75793b6703d1b05f96fe1065c06bd640499430d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.0 MB (250015692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:339acabe9aa1c17b694aebfed07a1d8eb6eee62513634ffad61d6f7ab7222e07`
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
# Tue, 17 Mar 2026 02:23:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:23:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Mar 2026 02:23:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d4761be313a06e0ee65741a8615e0eae6308a5cf9ffc27f5993ac0dddcdf81`  
		Last Modified: Tue, 17 Mar 2026 02:23:50 GMT  
		Size: 220.3 MB (220283699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:38995914a570b944ab606bc4891564bd53ca1f2a21dc7407a06bca26b95a0703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2363204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bdd8e91ca646860d4a7076d0db78ee2154e5ee51de61ad2cdb176af4837f217`

```dockerfile
```

-	Layers:
	-	`sha256:84706b0fed91c8422c9eba50af1df804efe95e9dd2b75aed820a023ab03ce446`  
		Last Modified: Tue, 17 Mar 2026 02:23:46 GMT  
		Size: 2.4 MB (2350601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edfa090fc7fffdf764585ae79f972dedb41dfa1e6904cfa46cfaa31d001a0f8f`  
		Last Modified: Tue, 17 Mar 2026 02:23:46 GMT  
		Size: 12.6 KB (12603 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:1b7a2494ebc822ac984a266f0afda5c64446c98eaa29bcb1aaf8f545d21eccec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246938166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52419c1a79a7a9f67bdae49154eac4fd80a0c2a4a22337bb8b8f77ba4c909547`
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
# Tue, 17 Mar 2026 02:29:50 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:29:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Mar 2026 02:29:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4484f55571509b2ce417ea79c2eb5f1dc3539432abdf24afdcd7c925c045146`  
		Last Modified: Tue, 17 Mar 2026 02:30:14 GMT  
		Size: 218.1 MB (218068457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c203990b96060f91d635cbeb0734fa22a2daeb2a229af7d9d695ab690a8b1a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2364027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6278c95f9050325f95562f7bef46fdc117b68e1d35533d95dfe61ac5d0b338c8`

```dockerfile
```

-	Layers:
	-	`sha256:1ef501179ce48fe07b9f946172cf55a54f725036e12a9d3540b6e90c66edb86a`  
		Last Modified: Tue, 17 Mar 2026 02:30:09 GMT  
		Size: 2.4 MB (2351189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df5999f2a1fbb647e96c178e6822d8436481dd4e627f1af1fb8df35415745510`  
		Last Modified: Tue, 17 Mar 2026 02:30:09 GMT  
		Size: 12.8 KB (12838 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:053e4e8a38c838fa91ca79bfbddd5943cff83287462511ec43e46b4c609de215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255306208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2fa5b8a976cae562fc8dc05268e6722af1b20cd3f27e93bc7e3071edf06ebba`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 21:17:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:17:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Feb 2026 21:17:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893c9fa42ed7f0bee9283e7b64b9a8d15ebc1cf2bc5eaad0d2dbb7f6c5af6b51`  
		Last Modified: Tue, 17 Feb 2026 21:18:06 GMT  
		Size: 221.0 MB (220999302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:faa00ffe3337cd22846dbc9ce1c51b86ec1d47492b3cb68a008d3e47d4c01446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2360168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c28ebec7e2e3caef91ab6d4c801dfa473ad99befa5c28320eed3cb62d02bc2b`

```dockerfile
```

-	Layers:
	-	`sha256:3308b8d8ce251c13fbd41c4d3b3280eb3630f2b8081809786a533b44997b297b`  
		Last Modified: Tue, 17 Feb 2026 21:17:59 GMT  
		Size: 2.3 MB (2347456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:959ae814da5ee1d5223713cb3bd03bc4399e882c5fdb4e32bcc123acbb68c980`  
		Last Modified: Tue, 17 Feb 2026 21:17:58 GMT  
		Size: 12.7 KB (12712 bytes)  
		MIME: application/vnd.in-toto+json
