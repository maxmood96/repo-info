## `sapmachine:jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:b299a584376302ef0aae2d207fdb84f52f9007c794deb1e6d94d079852feb72a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:a343d22fa6c13de5d54954c0f9f9e9a32664246352768dccca4e016d6eb128f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88730623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:becdddc383d40240e7a89dd376a37979f94a07197e065fe226ba2ff147acc05c`
-	Default Command: `["bash"]`

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
# Wed, 18 Mar 2026 17:50:12 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Mar 2026 17:50:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 18 Mar 2026 17:50:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dac3460ac0b27386294265c80e7a14d8e1d19733e824feba14fe91acfb447b9`  
		Last Modified: Wed, 18 Mar 2026 17:50:26 GMT  
		Size: 59.0 MB (58998630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bceb566c8d985f978b731a85e11f75324af1721716a7aaf85a22f46ba41d7a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2534817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b65f22d6009c3769a25726582088e934acd0ed244d15f190e8108f52e936628`

```dockerfile
```

-	Layers:
	-	`sha256:e168f08fbf9e0d0c3e438cd7b8aacbef70f92e6765361e9b60e02348e489929e`  
		Last Modified: Wed, 18 Mar 2026 17:50:24 GMT  
		Size: 2.5 MB (2524848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87ab1eec2cb5116a107d2a6d22cd3945b074508ba40ddf7fabea38294483f114`  
		Last Modified: Wed, 18 Mar 2026 17:50:24 GMT  
		Size: 10.0 KB (9969 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:2c41516032eb899ef6065ec1a6160eeeefd732a61264bbb6a61dcd13e2f64bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86876435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a955f910f145b88c5f10c650197cf86ffc0ff3fcc84b21c370ce87d76cac24`
-	Default Command: `["bash"]`

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
# Wed, 18 Mar 2026 17:48:17 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Mar 2026 17:48:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 18 Mar 2026 17:48:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1d2b07610bec53360f1c29ce285c4aaeea67cc31cfdd6b13c78cf66761e2ee`  
		Last Modified: Wed, 18 Mar 2026 17:48:31 GMT  
		Size: 58.0 MB (58006726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f241ae806e50ac2d7f356e0d612a60cbb6a2642dbd40e81aad0aaaa8c815a845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2535481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bdb3e3806311fd4e0bb3c97689747941b8ff349b7d674e6917671a54c8c3d32`

```dockerfile
```

-	Layers:
	-	`sha256:d8a97fdb1c5c7879b6d4ca282b06ba96b388414a33a47221340f8bf95a563292`  
		Last Modified: Wed, 18 Mar 2026 17:48:30 GMT  
		Size: 2.5 MB (2525361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4a3f4f555bf48c27fafab6a7b4ab07453f5108394dce72d55320ce29052b91e`  
		Last Modified: Wed, 18 Mar 2026 17:48:30 GMT  
		Size: 10.1 KB (10120 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b08a0aea75acb07c73fc5d7eabcf675694678d64f6c89cf23b37820d0eb3bb91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94467282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c5663301ef1fca7d7a63d4862b98ea73881a988c80dbbf3c8104c0e35e2022`
-	Default Command: `["bash"]`

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
# Wed, 18 Mar 2026 17:48:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Mar 2026 17:48:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 18 Mar 2026 17:48:41 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46195fa54c9f990340bfa96bb4f3b753fbaa3efb9f7f523790faa2106feefaca`  
		Last Modified: Wed, 18 Mar 2026 17:49:07 GMT  
		Size: 60.2 MB (60157231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6ae10e01eedab9404902295b4a3eb2e8cbf4bbb981a9c9bf051208fb415e29a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2533751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6da84b0718247714ea5c129642cd6e00d59eaf190d8e43d1c10d426465b116f7`

```dockerfile
```

-	Layers:
	-	`sha256:c4c33d903fd5eab9fbb06938c1dd3fa3435a619c134da92014cb094da09e6fa3`  
		Last Modified: Wed, 18 Mar 2026 17:49:06 GMT  
		Size: 2.5 MB (2523716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90d4cf1c771825553a136ed9d71d5bccb575ee98975a55223ca4595589dc5a39`  
		Last Modified: Wed, 18 Mar 2026 17:49:05 GMT  
		Size: 10.0 KB (10035 bytes)  
		MIME: application/vnd.in-toto+json
