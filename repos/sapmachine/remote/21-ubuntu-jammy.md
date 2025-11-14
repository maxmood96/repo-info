## `sapmachine:21-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:d3975aaaa85c1271081c54e6a95be3c8b933ea69e2cf956f2c1e14a07f99cbe8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:21a616f6c5a255e8d05e359b5486757094667b213b00518cd90c6208c7523b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244514695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501f786bfc5ff412ed731a107d4c3692e422aae5fba2b2a95bc75900284cbee5`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:38:52 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:38:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 13 Nov 2025 23:38:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097bf9a9077d690d696f2d941fc2bc0fb5abb1d2ba36db1789167874d63b1dc8`  
		Last Modified: Fri, 14 Nov 2025 03:20:57 GMT  
		Size: 215.0 MB (214977897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:02594520787999857b7ef5f681eda6b80dc2576346d59af713305b159ae242d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2639804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2fb6e34d7034fde9275219eb0dc6a795d6383b3f06ec56f2973deb3e75b611`

```dockerfile
```

-	Layers:
	-	`sha256:132e0a1c4be8c742307e2f08ef208a71d7cead2ac6bbfb471cd2853add167cd0`  
		Last Modified: Fri, 14 Nov 2025 01:10:03 GMT  
		Size: 2.6 MB (2629722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da4575e18d8f71d38ab6cb3cebbed99527670a6fab628d22efc33cd20fa8841c`  
		Last Modified: Fri, 14 Nov 2025 01:10:04 GMT  
		Size: 10.1 KB (10082 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:d0a8856d0e432ff544c0f157be604ccf9b933cc995573674e44ed901899c37ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240560307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba03177256eb4d6f5ab7687b07deafab4347118c8cbd3955714404603a4f089c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:38:18 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:38:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 13 Nov 2025 23:38:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce8cea5ccd757827a236795590437033b1ff723bda0ce5959ccfea89dcbd96f`  
		Last Modified: Thu, 13 Nov 2025 23:38:43 GMT  
		Size: 213.2 MB (213176430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1135dd8f93b1c73becc4f06575580150a7a99ef7830207cc35b942663095afac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2639686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a000ab268aee38116450efe8e863b0d1d318926286e9b02f11cc04a475b1c4c9`

```dockerfile
```

-	Layers:
	-	`sha256:56af009e2de16d7b0a11e53026c973e1843bf1ba555b60308d9eccd001e15967`  
		Last Modified: Fri, 14 Nov 2025 01:10:09 GMT  
		Size: 2.6 MB (2629452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9014e8c19c3bb865dd7e7903f60e90d8ca3911d39b758c4c76f5db9948af06c5`  
		Last Modified: Fri, 14 Nov 2025 01:10:10 GMT  
		Size: 10.2 KB (10234 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:4612fa9891b6bab2f08e50fb868387609243da7f9917676eb0806998f35cefa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250261170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:effa5e2125e07d6aced8eb5af78ab99792449f370b4acb7c5ec53cfcdb6b6031`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Oct 2025 07:06:37 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:06:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:06:42 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Wed, 01 Oct 2025 07:06:43 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Oct 2025 21:30:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3be6d9377084358bb79dbc96d7039f3ecf59bb5f0c80f8293572e08601ebb2`  
		Last Modified: Mon, 27 Oct 2025 04:48:45 GMT  
		Size: 215.8 MB (215814381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:22b8470c9ebe248b4ab77cff9e67da5a7c1c6fa3c22bf4e467edad524be3098f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8c522a59fdd96510ff7a156b8670166413c3bf4fa86d59192788eb8d378178`

```dockerfile
```

-	Layers:
	-	`sha256:f5facc3c6d0d972209e0a9a7076fd22135452c0809facb2bf6a79000f2f39fd2`  
		Last Modified: Wed, 22 Oct 2025 15:07:48 GMT  
		Size: 2.6 MB (2625915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60bf56efcb2987808a3b7fbb56aeada2392ac431fa500d1336640066d5f48ee1`  
		Last Modified: Wed, 22 Oct 2025 15:07:49 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json
