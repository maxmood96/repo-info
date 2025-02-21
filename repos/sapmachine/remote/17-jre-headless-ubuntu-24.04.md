## `sapmachine:17-jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:5844cc17e3394cc626abba8db14335e898756558a4cbb0c36d9813af49bab0a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:00d710c9f89b1f4c2b73dd2dd48bbe0366f5982d39861c1e53d002259abb0600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82760001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5659a1b6c71d05ad9ac3698570cf93a1256fac69cd11c4564272145d10ca67`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:8f1ffb4bcba4a3e28e5396a98dd8e7a341c7853bab69bbde84d66d6243ea9019`  
		Last Modified: Tue, 04 Feb 2025 04:49:31 GMT  
		Size: 53.0 MB (53005711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dd57cadd571182910bf162436808324e71eea10364fcd492c0686aab58b659f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2160529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402eea3499447ef3a735421aef4b6ac607d91fba265478d6cd6787303c990745`

```dockerfile
```

-	Layers:
	-	`sha256:5f42407f8483006b24fac3a90f4d7685f77ef5ed2622eaa42e3a338ac22d60f3`  
		Last Modified: Tue, 04 Feb 2025 04:49:30 GMT  
		Size: 2.2 MB (2150911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c73c5e831791cb8685f1defed06ba502e361879846f0ace6108d0c86f7f094c`  
		Last Modified: Tue, 04 Feb 2025 04:49:30 GMT  
		Size: 9.6 KB (9618 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9414840844bb9edf07ec0898436592e6a759964e431c14eac2b7919df6ee5c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81349804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f8770f49c15a9c435d32d5dfc93918a728e09863d950898f6f30f3063a01b2b`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:ab8e8e73584734ef9d30bc2007baa2059800c60585a57e7fc3ae5dc2f0e2b138`  
		Last Modified: Tue, 04 Feb 2025 15:36:41 GMT  
		Size: 52.5 MB (52456206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:15964b6e182fc16a5c19e2d45ffb71ba19ebfe81f30d32a3902f25f49ddf3520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2161140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec67a9f664d74a020e1df4612f1614f8bda9f3a864c0328da24862cb201e26e`

```dockerfile
```

-	Layers:
	-	`sha256:afb4e1111c9af266d3725cf907758f6c88657b51da5bd1b4d3ffa2f0b9024970`  
		Last Modified: Tue, 04 Feb 2025 15:36:39 GMT  
		Size: 2.2 MB (2151394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9def595592e01807dd1c1cf1c47bf1405c77a5dbc7011615c8be4cd35d87ca5d`  
		Last Modified: Tue, 04 Feb 2025 15:36:39 GMT  
		Size: 9.7 KB (9746 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:73aac2302dd01a299091530ad579e527e65c038acdb1a17eac9470f55c431b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88832384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d408c1812cf3991a952ccf6b1ad952f64f5d5add30d75385bb096fb0f782effe`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:7ca5af8afd17dd9222cffbdc87c02cd88cb4467b6d0f963f908c7366e219d915`  
		Last Modified: Tue, 04 Feb 2025 14:53:57 GMT  
		Size: 54.4 MB (54442560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0c360e8f9824e33168418d6b55ee9031b6d67b268f310d34c4d73c3790a4a3e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2164473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b140035234bba17a9c749c33c103002c6f3da0034528045cf8c9778ee2a9a7`

```dockerfile
```

-	Layers:
	-	`sha256:c7fca8ae5f7003decd5004c00c7f32869a6fddf3fbb873b2871dd8a7b1d6bf10`  
		Last Modified: Tue, 04 Feb 2025 14:53:55 GMT  
		Size: 2.2 MB (2154799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eae12faafcc2415bd84112b2cef28dbd6f323ac37ae950cd9e60215d09cc3aca`  
		Last Modified: Tue, 04 Feb 2025 14:53:54 GMT  
		Size: 9.7 KB (9674 bytes)  
		MIME: application/vnd.in-toto+json
