## `sapmachine:11-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:d49e0bccd068a3718ebbcfefedfa27e7dfab65a1669e28a294d0b05cc340637a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:fccc579c68fb8d3fd9fe41e62fd2fc55a20d4afcbdaac0ba47b23b8bf504cf84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82490097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0553267aeea78c83cf7099bfe34ef114474a86abf2bba6bff9ab85c8226ff63c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984955d4e68dba0b2f2936df84c7fd917ab47463bfbd2f98092707f21597c12b`  
		Last Modified: Tue, 17 Sep 2024 01:00:49 GMT  
		Size: 52.7 MB (52740269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:df3a86cd3a327221f2cc338add34ecfde0f54bde2252195789d0ab2f30e9d47f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120449ed896b9234330f42aacb3379751fb03ec37d7f7bcb8aae729d990b89d3`

```dockerfile
```

-	Layers:
	-	`sha256:81625567d815830a96ed63664cd97eae2f634e96bedaa08190d610c149585059`  
		Last Modified: Tue, 17 Sep 2024 01:00:46 GMT  
		Size: 2.4 MB (2374825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f36dd4577550c140330aa248fe9fdd63b886126d215d5ea55d7fe98a1500b95b`  
		Last Modified: Tue, 17 Sep 2024 01:00:45 GMT  
		Size: 9.2 KB (9216 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:b0959a31cb5773b34f05a25c22ada823605bc7a212cc9e598c0dfe05695bd4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78524598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2618588f02a1a297f2e77228a7fb71cd287417516ab31d67c5b2b6f5328638a9`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd49de86346e194a7052463ea11e9a8e186cfef05b94a9b847fa94b21b2f12c`  
		Last Modified: Sat, 17 Aug 2024 04:43:35 GMT  
		Size: 49.7 MB (49680912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a8abcda23f68c845089b67edbbc32330b1049c4d61163a0350e640a71a791190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c690743887dcb8bf751919d01c7f739d5cb53de191b01a8c282a4df3488dd0`

```dockerfile
```

-	Layers:
	-	`sha256:ce765384fd9e03cd82aed97ea6193133004dba77d88abd3bd2de54494524338d`  
		Last Modified: Sat, 17 Aug 2024 04:43:33 GMT  
		Size: 2.4 MB (2373386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87349e57cbe4c9c4056131d236f943e5870b3e113bad171a8aeffb2148961b9c`  
		Last Modified: Sat, 17 Aug 2024 04:43:33 GMT  
		Size: 9.5 KB (9542 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:4f0972d9928a172785afb91a576cb7180fbd17cb173b4b9b93156daa145bbeef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83606828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585c2036240def12eaab7fe0c4b7154c39d1b0259774d74f7bdb8a3658d28a37`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f16ff2741334b0be5d9f311961a37c8bd0feb2974974ec52a327bbae3866e29`  
		Last Modified: Thu, 01 Aug 2024 15:42:28 GMT  
		Size: 34.5 MB (34507572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b0dadf2ea1fa9eea005bc82e9248b57c7bb995d5df545efe3fcee72b2e0094`  
		Last Modified: Sat, 17 Aug 2024 03:30:43 GMT  
		Size: 49.1 MB (49099256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6a96dc48bfb01ac88fd301ae04f27423c290a2891ef38e2ccb96543dce80d90e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dcd7e5642f8a471565c13b33aeec226e62cb40eb98625bf1b76b45558bc7636`

```dockerfile
```

-	Layers:
	-	`sha256:00c5160a625493b702bf9b9433ede032fb65fb18e2dda2f33b91192880084151`  
		Last Modified: Sat, 17 Aug 2024 03:30:40 GMT  
		Size: 2.4 MB (2376222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e07cf9a5d79e9b0dd4f98d7622ea08402f288eabfd1fc1c8233731fc660024b`  
		Last Modified: Sat, 17 Aug 2024 03:30:39 GMT  
		Size: 9.3 KB (9267 bytes)  
		MIME: application/vnd.in-toto+json
