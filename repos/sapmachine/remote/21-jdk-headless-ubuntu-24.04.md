## `sapmachine:21-jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:6fafb84ae7679221fc84545d976c4e2680bc1690c01e1524c8ee8aaf803d3b7e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:8314d1b8f538d567a882e66c2fe7a466b5ce1ad16b288be882bff012239e61c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243843854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a66e1dc8de853e780f1ec6ec309485f61691335f717ca4bd672159e3db73413`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71711c9276ce706b0850174d069029aee39561177ba2a61fa4086411d106db18`  
		Last Modified: Fri, 10 Oct 2025 07:33:53 GMT  
		Size: 214.1 MB (214120707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:48e071033bf6a7f33e697fcfe39a334a31363a4133dd37d51d7042d747fb7027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a7ab7bfc879f1aaadb86b1ade2a8e07bb5f66cbe8f6c4f1c7462b7157ed6a3`

```dockerfile
```

-	Layers:
	-	`sha256:97ef88b8760995c0143c9e396ac3711309ca125aeee52141617715dc6762b948`  
		Last Modified: Fri, 10 Oct 2025 00:08:58 GMT  
		Size: 2.4 MB (2356331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:417d7f5cb68e3da9b6985b7cb7964c3f81a7d39a71cf02c0e6bf84947474f22d`  
		Last Modified: Fri, 10 Oct 2025 00:09:02 GMT  
		Size: 10.3 KB (10264 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:8eba0f005c87fef14d7e77e0d6fdbebe01c57f3df477e6992db0ac840a7dcaea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241277249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ef6c64a8c50f7de8f74313306b2adc7dab972bcee70afc53235f91473883ac`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Oct 2025 21:30:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f43ac5511a77c025d6ddfd43d06c2d0e036b85a74f638e11d889afead1e191`  
		Last Modified: Wed, 22 Oct 2025 00:05:36 GMT  
		Size: 212.4 MB (212415537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e0911b7393f8ef4d25be89807ab1ca4b9d668a2438007e6f124274a419771ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2367254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab58e30910e5a85222592d52def0f238a451f1bdbc26d27c8fb584876ac0ebcd`

```dockerfile
```

-	Layers:
	-	`sha256:8984c494681c4384c1ff0c9889e46a7f2e4ee2f9f50057793a0086501b475d60`  
		Last Modified: Wed, 22 Oct 2025 03:07:15 GMT  
		Size: 2.4 MB (2356838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f892106b4993b5b66f7a95eb7e428f6d894652314ed8eab16c95f8e8bec4ceb`  
		Last Modified: Wed, 22 Oct 2025 03:07:16 GMT  
		Size: 10.4 KB (10416 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e0c0fb407098cfed126128fc2e0dce80d9336ba99290aa9bbe388e730a64910e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249183626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821158a0e34453d60d8415b6dd086ba17968fdbb33beef54358aa9a4e168a39e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddaa48029ca55fd50c7f862e25b5425a2703bd2675ef40b91a986dbc8c1fb4de`  
		Last Modified: Fri, 10 Oct 2025 21:27:32 GMT  
		Size: 214.9 MB (214880101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fa8839c054489a9d8876446f56b1d728442bd815bf1ae338da7d1770bcf725b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2362717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a879638f7446964935b396381d8ac26a1ef44f041f498e7a622de1b3b8a4dee3`

```dockerfile
```

-	Layers:
	-	`sha256:a19ac3f58f1ae842289dc0019c117d9de41be7cb0354787ce4b244bdf61062cf`  
		Last Modified: Wed, 22 Oct 2025 03:07:19 GMT  
		Size: 2.4 MB (2352385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9709e40d7fd4a4530da149ac000ae49916f334780a071cc44df7fc8f40af3078`  
		Last Modified: Fri, 10 Oct 2025 00:10:53 GMT  
		Size: 10.3 KB (10332 bytes)  
		MIME: application/vnd.in-toto+json
