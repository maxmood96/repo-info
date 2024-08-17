## `sapmachine:11-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:439f72f86fee80fd06de1a7278f639e72c4e4bfcd8cdf479aca04a73f915402e
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
$ docker pull sapmachine@sha256:4572c1fed6acb4b23a3dd55a2bb08082325ac443f41b80c700f353c7ef7559d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80043965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b362eac7097a683d0865df1d799aa3f8b198a269cbc9763c16a5156a3de1a425`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de39369408ab0122719b608ea75ecaac9e85be0700fbac570698f644f06b80a1`  
		Last Modified: Fri, 19 Jul 2024 18:00:11 GMT  
		Size: 50.3 MB (50338812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0e43583d11b78184f7785e0f5996dfe66c2272cd6f809013297429cedf869934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6400c8f622eb069aa99bc470a9efdd20e8a76899900bf673712826644e98228`

```dockerfile
```

-	Layers:
	-	`sha256:b3eaf6123775c3e7a5affb7a4667c1a1aac0c6bbf6787ece2ac87bd766a12735`  
		Last Modified: Fri, 19 Jul 2024 18:00:10 GMT  
		Size: 2.4 MB (2372267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23690b52cb7b8bdf07680692b133966c9539bea7b4d06404c5eabe0a538fcfce`  
		Last Modified: Fri, 19 Jul 2024 18:00:10 GMT  
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
