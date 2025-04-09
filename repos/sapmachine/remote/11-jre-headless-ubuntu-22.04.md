## `sapmachine:11-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:09ba8bd1bca5b0a2abb5857fd7bb89fdd6f4dee2f8ae0ae00ea91f6f777430f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:24636f227de94c37e7dcba95b18593fa5c042944bae93709d1ef7ce2e13e1454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78313132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae1eee087952d44cb310741f52b9e0e9a86c7be7ed4d62838170f934db81920`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:19 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:19 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 27 Jan 2025 13:39:19 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 27 Jan 2025 13:39:19 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:19 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 27 Jan 2025 13:39:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d220b3c759723d24e04a63231c2d35645747c1fb1828f92b9ae419bcbd6efd34`  
		Last Modified: Wed, 09 Apr 2025 01:22:01 GMT  
		Size: 48.8 MB (48780767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:713e5648bdf86a9757c0929c32d9785b16433c51ca0b2514fe17233c0951ce7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332d2a622be1fc2e2aa97a244976978c76660ce0951b0f4b92f4b520c570dbc7`

```dockerfile
```

-	Layers:
	-	`sha256:ff125a5639bfb71f1f5bc6e0731a2f4f741ace6ab60e20940704e9307d02a645`  
		Last Modified: Wed, 09 Apr 2025 01:22:00 GMT  
		Size: 2.2 MB (2170998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc0c8a31695e37f8ab9bd0379ee6fddd78f8dbcc719f4e9aa343e0da4b36a905`  
		Last Modified: Wed, 09 Apr 2025 01:22:00 GMT  
		Size: 8.9 KB (8932 bytes)  
		MIME: application/vnd.in-toto+json
