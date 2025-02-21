## `sapmachine:17-jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:219681e5b6b46cc95245f7af7e0bec702527e7950fc4a27d2d183ab4286ced6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:e12ba0a1fbd0443475218e4ef93cc67e2957f102bebc3eb38ef1ee602eb46b17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (83954636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f517d410ec6d37782dea70eecfa5249a01c127a81b146a8e4bb3f3bca0ab6262`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6fed1e88515d5dce57005f39dfdd4f3789372168d44bc0477f38d65ae1dd90`  
		Last Modified: Tue, 04 Feb 2025 04:49:31 GMT  
		Size: 54.2 MB (54200346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4373096c064bc78ae7ec9250539b4621e2cee05245712c7245c4bd473d8e8ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2397235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a5da4185d7a7ca69a7ff0fafab993b35b60ae4eab50f1b8c639c20eab78768`

```dockerfile
```

-	Layers:
	-	`sha256:7252c771792d6c545478721d4e5bbf1717da2a8e849159e7941f9b7871b11be5`  
		Last Modified: Tue, 04 Feb 2025 04:49:30 GMT  
		Size: 2.4 MB (2387765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c65355ffeac42033714b988898679d332360fb957d1c65b4d6d0ea8d8a466f4f`  
		Last Modified: Tue, 04 Feb 2025 04:49:30 GMT  
		Size: 9.5 KB (9470 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:397856ea90a2902122fa3ba8fd6255d4bc4574b99526e87ec45a45a2fe8d035e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82544758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a07dcda550a6094f8fb963b882b4612ebfa0ef987d1da36dffedfba35926a5f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeede52bac7581278488922ec3cd7375cabdb3f0f37853550cefb84d002c1154`  
		Last Modified: Tue, 04 Feb 2025 15:36:02 GMT  
		Size: 53.7 MB (53651160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:46f895d6389242f2f502f5f9d7096e22eea4627c28271f75e3d2d834b6324784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2397853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad3b41e35baa60d4b101d93031f99cf32fa124a57132f254a67bcb6baeaca7b4`

```dockerfile
```

-	Layers:
	-	`sha256:d6263c61c382c36c26d318f3aa5677f1bbf2f79244ceddaa32792d1183e3f425`  
		Last Modified: Tue, 04 Feb 2025 15:36:01 GMT  
		Size: 2.4 MB (2388257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43fe489602833af2ffac0d6710c3fe443d4ee409f5245d4499250841686e71d9`  
		Last Modified: Tue, 04 Feb 2025 15:36:00 GMT  
		Size: 9.6 KB (9596 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:9d907a789ef23d21c3e1d23f8404f23318521dfb80df57de26c15a70a31300ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90211576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7d6bac699facdb808cafdcfe08289ed0cf4379d0eebb033d77f92f5d69b48c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bbc622bbc8f238a43b4f25cc2591873b3fcb306c9a8b44e7436a9d12b6a59d`  
		Last Modified: Tue, 04 Feb 2025 14:52:33 GMT  
		Size: 55.8 MB (55821752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a183eb90460caf091aa96815b92fdb546506214a8222ef3bc5a61816b0d5e058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1494d9aa9048fae0f9127459746badee1508cf67a11b4034bea3daf4511ab5`

```dockerfile
```

-	Layers:
	-	`sha256:f40a0742bce6cf36dcfe9a98c35935529e7a707c72781bc695e2b2fd3f79bd14`  
		Last Modified: Tue, 04 Feb 2025 14:52:32 GMT  
		Size: 2.4 MB (2391716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a850ff7304723e168eead3a72eaa4ef5dfddebaed6e5978d1288100d66d5bca6`  
		Last Modified: Tue, 04 Feb 2025 14:52:31 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.in-toto+json
