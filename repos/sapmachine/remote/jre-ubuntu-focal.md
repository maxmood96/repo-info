## `sapmachine:jre-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:fe116b2a4911e73b6ea2ac1913c1e6e907547ca62ad02676da16956d70143ad3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:eddbd8309ec8da5a75f43f0a884ab9f5f16facd7535da506882ea456e27c4bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86427962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de547db0aded7cbd36a730bb8901f3ac3ecb63e7b2db7ac560c9751e575dec5a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Aug 2024 09:26:46 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:26:48 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 13 Aug 2024 09:26:48 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b0ae34ce1059a386fe04fc7f8999ce8327f790f76ae91e84023b5e92a069bf`  
		Last Modified: Fri, 20 Sep 2024 16:57:43 GMT  
		Size: 58.9 MB (58916193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ebacc96a781c52d61f0d54b504a561e9a3a61d6956a77221687c4e80965dec70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 KB (10881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:effa7279c3269812cfbaf8a5d8bd5047dabd9469951051ca0400d5994d5bf4e6`

```dockerfile
```

-	Layers:
	-	`sha256:e300aeb108c9cbc49ab35246afaf618ed504b64a8df9c1db5d57fe37b09914bf`  
		Last Modified: Fri, 20 Sep 2024 16:57:42 GMT  
		Size: 2.4 KB (2359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97e256415668d7144c65ad3276b18c0be65339e5ba80d017bc6dd8dbb6c30f41`  
		Last Modified: Fri, 20 Sep 2024 16:57:42 GMT  
		Size: 8.5 KB (8522 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:b1585066c80a08c0ad0866c5e12de6e6b79855dc37ef7ef943d5940bd7c4920e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83922366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2c22ebfbf27eaf33f4ccbda66573d57299a1ffc44688cdd9627d4dfdbfd90e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:56 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:27:58 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 13 Aug 2024 09:27:58 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a1df50fc4815789598fa24d3ecacb70451e506447ab9e45665024b9f3f0233b`  
		Last Modified: Tue, 13 Aug 2024 10:23:55 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e76b020fd122cc5fbca58885fba5091fc510daec4303ca9b181ca081111b4ac`  
		Last Modified: Fri, 20 Sep 2024 17:13:40 GMT  
		Size: 57.9 MB (57948149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:86e14dee8b75673be359f82eb8fbf0cdff553227bd10c68b6c82753582844076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2290600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611f8220d9fb95e5907b6c62ca4430c6f86ca717ae1cdb336d7d7ae9c51cfe13`

```dockerfile
```

-	Layers:
	-	`sha256:746e21860f2f241275bf9886a111d59098cb6ea8e0b9f188543b4c0ab6a23920`  
		Last Modified: Fri, 20 Sep 2024 17:13:38 GMT  
		Size: 2.3 MB (2281777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db80493ef12502a2cc74d6bbea0231c030d4707f321556387abc8a4fd0271667`  
		Last Modified: Fri, 20 Sep 2024 17:13:38 GMT  
		Size: 8.8 KB (8823 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:31cde2f6a83a80f22078880b389759220f0671efd2d399cff9a975ea8da3e9be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92012451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f389d638a84e4d70566b28f403e141693f45e484cf14f536c6a3e6c5ff192c85`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Aug 2024 09:30:49 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:30:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:30:52 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Tue, 13 Aug 2024 09:30:52 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dc326ec944b7858d5d87a7b0cb86c8d0aacc5f789574834b5e1a503f685abba1`  
		Last Modified: Tue, 13 Aug 2024 10:24:07 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bf8a4444b2d78eeedb25db35bf155cbcb5bee4bf7da7636ed92ec956c31606`  
		Last Modified: Fri, 20 Sep 2024 17:19:17 GMT  
		Size: 59.9 MB (59935311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dd952538e90d15c7ab892a403eff2cb6b28bc8312420428a3156293348a1e4c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d963b1efa47eb679ec9517fdfeecc4ca33590316262d55e8911d46807d53b3`

```dockerfile
```

-	Layers:
	-	`sha256:bcb6b89366b1979da67832e71962fb5dfb60bfebaaffdb3e20a2d82e9293f3b1`  
		Last Modified: Fri, 20 Sep 2024 17:19:14 GMT  
		Size: 2.3 MB (2285906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b2b43eefb9bc834ffa75ded9c55a7da304d87c3deace59f93fe269f1eb9ee5c`  
		Last Modified: Fri, 20 Sep 2024 17:19:14 GMT  
		Size: 8.6 KB (8559 bytes)  
		MIME: application/vnd.in-toto+json
