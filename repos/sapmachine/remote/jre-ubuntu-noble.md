## `sapmachine:jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:70247bfe3c888c9b0b4da6d5aee5d5d52a560395f9d28b01cf65d82b5023b6b7
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
$ docker pull sapmachine@sha256:8b514eb01663b748a463517cb31e8744eba5c26d6314ab4b8e2cedc03810975d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.8 MB (97795433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3585652fa0f8147372ca696ffedce342f3916d1f066d60865074fb83f9363a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8fdf661188af0eecf56c0937ff3b304245d5d6d7822a595f1de7d0467b358aa`  
		Last Modified: Mon, 05 May 2025 16:36:33 GMT  
		Size: 68.1 MB (68077904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9f08c0c3c03217148972241b2ff5c1e5288a18cc868846846e2cec6ccee13be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2405276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a20ed7813711bee1426462d73a1749396466dca10d9b75137532accf55fefd`

```dockerfile
```

-	Layers:
	-	`sha256:4088d1ea75652e2464e542fbec3670321adccfe3ffdfc87613312d00c8f368f3`  
		Last Modified: Mon, 05 May 2025 16:36:33 GMT  
		Size: 2.4 MB (2394850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e1c83e176202f5c3ab1a47419807b562b7b0714485bd61b91cbd217cb12c81c`  
		Last Modified: Mon, 05 May 2025 16:36:32 GMT  
		Size: 10.4 KB (10426 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:620929796b888e13ef31f50f1ed15a0ce5e8cc9469e8265aff50dc6ee2730a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95966613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d357d04c4dc52450bdb5d5dae64d06a2b2c9f0eeccaab51770cf076abb0186`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c30f98643da0d352edcca71cde7f735752c83d594d7de2874f1f4041d8a43bd`  
		Last Modified: Wed, 16 Apr 2025 16:15:39 GMT  
		Size: 67.1 MB (67119655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3266738013fee70682645f1efa7629d30e56c857e933bb93df42e0576db295d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2405961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d56733d43e4a672496b06a9dded203e7f28a02a454708f4440e4c700dc2275`

```dockerfile
```

-	Layers:
	-	`sha256:41a40e2ff65087a3a9cbecea20ffca71754a20457f5cc4190f87427a339c588b`  
		Last Modified: Wed, 16 Apr 2025 16:15:37 GMT  
		Size: 2.4 MB (2395371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0fc89f8ff79f1561cbec224e153fd8ab22f7bc99623537dae7b42a316f0b8c2`  
		Last Modified: Wed, 16 Apr 2025 16:15:36 GMT  
		Size: 10.6 KB (10590 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:77d258e7c430c0b4079611145c6876dd6548ced07a00ed88436817498d891a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103800020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f192ed028e2c35c558a701e1ae0b8a8812cd6da2fd6cc0ab5cd6fe11016b3571`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:11 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:14 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Tue, 08 Apr 2025 10:46:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bd63beac845f37c736215c04ee770f025ed38418a9d2492df3f617e7143592`  
		Last Modified: Wed, 16 Apr 2025 16:19:08 GMT  
		Size: 69.5 MB (69459153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ea03ad8116864e578352b4357b3a4338476b7b095158c5d65b22ca01c995d018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2408685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394a1ca75361670ef87fdb029e91b5021a71d84b5eed8174f96840bf064ec92b`

```dockerfile
```

-	Layers:
	-	`sha256:c9bf2002d465434688b6cf41753377304ee11b200086752fde16d32db197e238`  
		Last Modified: Wed, 16 Apr 2025 16:19:05 GMT  
		Size: 2.4 MB (2398185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c0b3c7fc65c422d84998c53f9feec41ddc60ed4087c9fe9421cecf7820b49ee`  
		Last Modified: Wed, 16 Apr 2025 16:19:05 GMT  
		Size: 10.5 KB (10500 bytes)  
		MIME: application/vnd.in-toto+json
