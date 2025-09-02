## `sapmachine:17-jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:9b9c51497c7de8d7e215226d3b71cde7ea9ca7cdbf0428364e33a739eb7d5fc2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:197be1863dcfc7247321ecc81d42383f8d8d2b6c75f5f0036c8e7a54999b62e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (229019987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98318f63960a4b1232d043d714b86039cf8c06a99401c94faa3bfe071e3c1f07`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a8d3aad0f9130a589f8d39410129cf6d81473e168a54950dd64c095b0073b9`  
		Last Modified: Tue, 02 Sep 2025 04:03:33 GMT  
		Size: 199.3 MB (199296923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:77a8814d8b647b3bc55d64e3a3b749836e374b34f7a8df17c6ce61b89254f3f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2364745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:625bac4d8c2b9e4c096d700f9802aa05208ee7b3dd8c398dbcde00f0d3b0fe7e`

```dockerfile
```

-	Layers:
	-	`sha256:9ca090290fb821ba1b5309699f1efba7aea3ea1bbfaab7e8b5a7ed04e601b5a0`  
		Last Modified: Tue, 02 Sep 2025 03:05:28 GMT  
		Size: 2.4 MB (2354468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:177a7fe2eb8a5cea218c9bf79001e912d8ca62739b397c6b00484a189277910d`  
		Last Modified: Tue, 02 Sep 2025 03:05:29 GMT  
		Size: 10.3 KB (10277 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:cf75ca828f21f8c7ae6557c05469a0e5ec7a7ce07ebdcf5ffc44509d8e2500f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 MB (226871504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c321329b1a7278ed4f9ffca050bd05a47a1e03048c0b7329f9a001dc0d68a577`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e1094488cc054905670381d1ac74a51c9f36d644a02a4f7115980ddefcea47`  
		Last Modified: Wed, 13 Aug 2025 16:47:38 GMT  
		Size: 198.0 MB (198011127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d4068adecfaf24d0baa0d8fa3e11281e07038ea320fe0da8c7be6f2c190ce005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2779a09a7572afd4c90c97ff16553b197ca42e9a3aed9599d7f5d1015417b349`

```dockerfile
```

-	Layers:
	-	`sha256:47c397966c712f41ac6d99c4872b60e0196e679b4bb3a797bd102a085a94b640`  
		Last Modified: Wed, 13 Aug 2025 00:04:51 GMT  
		Size: 2.4 MB (2354975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:035ca21667bf3b80f2de5e83550d770d55cc4db2cdadfaac0b3041501fbc4e9e`  
		Last Modified: Wed, 13 Aug 2025 00:04:52 GMT  
		Size: 10.4 KB (10429 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:650130d56d2d129682869b001f6226ff5ec366bf123b422a924a5deeb6143630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234204187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4179b96d3b147722e3a6a1e401fc440fd721c2d1aaf4fd0f94c4683b648f1249`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:e2ae399c3aa36bf07b7d3562a21b9ad89f66ae6e03733ed0edcdcda5bd391c60 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:403b01240f845337685ead3abfb0228bb1d1b78b076d609aa20f4733d260f58f`  
		Last Modified: Wed, 30 Jul 2025 11:30:48 GMT  
		Size: 34.3 MB (34329650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d8efd726492aa10b73d11fd42a1886bd72b281cb65e022dc30839cff13805d`  
		Last Modified: Tue, 12 Aug 2025 22:53:02 GMT  
		Size: 199.9 MB (199874537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6c17105f29183404fb579fc2fdce6c10e43fe8e1e95ca1336f774a2e23758a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2360867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee42e66e283ca4a94e2db925a71eed5d192e33d7bd910fd513aa1288b4659f50`

```dockerfile
```

-	Layers:
	-	`sha256:5a9edbb44dcc16aa790bca3c3170ea5f50075abe435c93fccff16f0efb04e09f`  
		Last Modified: Wed, 13 Aug 2025 00:04:56 GMT  
		Size: 2.4 MB (2350522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e183dfe8e7e2ce2cc13de7f4130d1c5bb27625429b078d8e67d86389e93dcff`  
		Last Modified: Wed, 13 Aug 2025 00:04:57 GMT  
		Size: 10.3 KB (10345 bytes)  
		MIME: application/vnd.in-toto+json
