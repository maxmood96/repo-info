## `sapmachine:21-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:50e8666945adb979ada8edb70e37681ea2a94794138d74697695fe007bf92487
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:f45941bb52ee75f1b017bd4999053ca6ab253fff77d5f6cf35ed2706a532e281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89361199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:763b276b272aac13d370a3e38bcccdecf791622138f7984eec718ec99b4ba181`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fcd8ea1c393aa4a9458ccf0fc51e4b0bbc973cbdf35dabb30169c8dc32abab`  
		Last Modified: Tue, 12 Aug 2025 18:07:04 GMT  
		Size: 59.8 MB (59824206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f8e3f80fcab0e2c43c4eeb153bc605af7b9c137249fa658ac3902d6cffac4634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2555021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe37e517a2a6e344b199e9ff512761552b91d94c93eb466012f7463989e3cfd4`

```dockerfile
```

-	Layers:
	-	`sha256:6ece9e9292975e89a87f4b0fd28db3140326afa42d446ad64ce0926db6909486`  
		Last Modified: Tue, 12 Aug 2025 18:09:07 GMT  
		Size: 2.5 MB (2545541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4fa32f698c4249e8c5516075f84c0f5dfeda09795a7555e26fce0b34176629f`  
		Last Modified: Tue, 12 Aug 2025 18:09:08 GMT  
		Size: 9.5 KB (9480 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:2402d5b7e85a13f1b72bf540fa69f0cb3b350e59be1cfdc206a39d25c3202ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86304423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de33a678a474edd6e74c6feae46caf137e08d2152bb89254ef7eeccaec8b0ee`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91588faa2c55b4ab183447c0c506ccef1ecdfdf3aeaa91cc1f3ecb63967a0c9d`  
		Last Modified: Mon, 18 Aug 2025 15:03:00 GMT  
		Size: 58.9 MB (58945176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:48f95e8a20155bbdfeecd7d58743a96cbf4a740b18f1a887be826348849519f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367b18c72e1a549f22c0779820fddb0e8635ba1aad25e8d7bfb35088a3fddc86`

```dockerfile
```

-	Layers:
	-	`sha256:8ff48d4c2dccae0a9c79f6ae66fb73624a6ac3bed1c72ffc4d5ca95aa4f63537`  
		Last Modified: Wed, 13 Aug 2025 00:07:49 GMT  
		Size: 2.5 MB (2545247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e1f044826c9fc205ac64805daacd3da4c670b6b820a0c82e54d866729bfe7e9`  
		Last Modified: Wed, 13 Aug 2025 00:07:50 GMT  
		Size: 9.6 KB (9608 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:720a24eae89d43bc749952bac495f68e7574e4d4360e3366dcea5207247b5b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95384544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68506e7e09a932a82979f18c7db7fd1f772823b31d4c5fcc53ffc1b519f6f64`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3b479f49bcbb4e7541030b6218607a3d1af43ad8828ce8b2d576492ddedb42`  
		Last Modified: Tue, 12 Aug 2025 22:47:58 GMT  
		Size: 60.9 MB (60941399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5ff19c89e327a83722961376688e0fb54c745d076babd00903420689555f48ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91fe08b9d1fc311bfa8d5f86c40de22d8da40fb0cd74d5d421f39465aabe2a47`

```dockerfile
```

-	Layers:
	-	`sha256:83973a31de35e4472988c75c0bec8fd611c771ecd7e8f2cb0b2905239981ceac`  
		Last Modified: Wed, 13 Aug 2025 00:07:55 GMT  
		Size: 2.5 MB (2543668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5a8730ee032e4906550a1a3e47c691f1f45cfed61486eab58d21fe5c40c8fba`  
		Last Modified: Wed, 13 Aug 2025 00:07:56 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.in-toto+json
