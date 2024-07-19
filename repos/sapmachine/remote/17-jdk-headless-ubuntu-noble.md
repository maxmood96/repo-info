## `sapmachine:17-jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:63a8ab445ca431055921f5a6070c9d8f5b6ac1b9fe5782be2cd60b14dcbbb971
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
$ docker pull sapmachine@sha256:d6425286ff99cd4e23cffa2e607477073b699122bbe553387f302958e2bae351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228951816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834c13b210f676edf5f53ebf250a598b95fc965ec98b4e4441bdf721e0d283e3`
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
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46814cc80b94b82e2bbe4c0b1e18fe611e341f055ed8b5113fcfa22378eb68ff`  
		Last Modified: Fri, 19 Jul 2024 18:00:35 GMT  
		Size: 199.2 MB (199246663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2187ae5fe1aad5f9e402025ebd61c949c16723e88668b98aa2d8e2b51c435715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2216510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e607e0d701f98c7c594bdbd382cd65c3f9efdc03b39ab85896c86605237c42`

```dockerfile
```

-	Layers:
	-	`sha256:67c7ec0efe22ade05660f320a17a07f1b52713aab097b8bca843768a41b45034`  
		Last Modified: Fri, 19 Jul 2024 18:00:31 GMT  
		Size: 2.2 MB (2207145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d60f9b570b3fb2eea958ac2e8cff85c420d2764f41d4463a7f7f63549b8f69b`  
		Last Modified: Fri, 19 Jul 2024 18:00:31 GMT  
		Size: 9.4 KB (9365 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:03a1efbe4d7969f1902b8aa9f9f7642f6f74d9ae1e4288c5d590788e961c9c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226583540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bea40687fa5aa576aea97418b7f3eb3bb42ad896e9a8cfde634b91b787461cb`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161ead3efa3b59da35a32b5bd8f95f7d47f55ce15eba9e34ebb58cdf788f2451`  
		Last Modified: Wed, 26 Jun 2024 00:16:02 GMT  
		Size: 197.7 MB (197740497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:24a4982adb1649ecc8a049e586cf04ac04584df6d78f71824f1347a0930af6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2191625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f188d0a51c4f5b509a8f43a5020f96801c527c87d7cedb2c96c82378dfe4caa`

```dockerfile
```

-	Layers:
	-	`sha256:97526332b50883a590eef2abd274e94963defc9524c627750c9e97ca8204c7d1`  
		Last Modified: Wed, 26 Jun 2024 00:15:58 GMT  
		Size: 2.2 MB (2181918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8741222ef29db503f63b720af94dfc3a9f9631bd593869c7434b378cc3bb66e5`  
		Last Modified: Wed, 26 Jun 2024 00:15:57 GMT  
		Size: 9.7 KB (9707 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:4cc90eaf5ae8be23ef8ba010c860d54063616ffa58f5d3154ccd4480e746eb2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234623262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff272776729b602f34e288d48868872dd438e777df20d2bac784a93376e1af21`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2e73aedee08c22b90b8f65673f9ec6d075ffa84a96c74b8a45c752f0095386`  
		Last Modified: Wed, 26 Jun 2024 00:49:04 GMT  
		Size: 200.1 MB (200117233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2c936a353b152ba49ce4884c9a69ec93a051183545f546a46eee5dfc4476d422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2192805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356cefb3b6bd00bdc62aa285dd7f6bd6c7fbbf032c208d8681f37d1290badbdb`

```dockerfile
```

-	Layers:
	-	`sha256:a18f7a17e0497bfeb17eb9d82eff72b0aaf258fbe92c662a8c8ee700eb96544c`  
		Last Modified: Wed, 26 Jun 2024 00:48:58 GMT  
		Size: 2.2 MB (2183373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4acdd003e99af7110523cdc4c786381fb4845bb67a3a28966808817afd30866c`  
		Last Modified: Wed, 26 Jun 2024 00:48:58 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json
