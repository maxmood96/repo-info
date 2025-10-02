## `sapmachine:25-jdk-ubuntu`

```console
$ docker pull sapmachine@sha256:51f168f70734ad8db6c90cef4b324d3c62867b55ebf3374ccc91fe7320c2192f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jdk-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:c54b4d4a5b2de9d467ef0927a23024d22301bf59d46ff98c6ad10b8ab6f5dd4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.3 MB (263348064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6521943d3c5317530d904ce6bc63a6c82034b91ef731abea313d2ccf12beb764`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e0d94b1583917327229d8b4b4a26396c18ef7e17839dbf460e61d90c4f4b5c`  
		Last Modified: Wed, 17 Sep 2025 21:25:09 GMT  
		Size: 233.6 MB (233624614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:daa5a81cd6411d5cb6f26a6f9aaac4a7930304aeba3964e56defa5f46f4b62f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2612998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1dd9b4699a0aa93c528e4898d48a981371f379404d0ddc87b783e1c8b8c9db8`

```dockerfile
```

-	Layers:
	-	`sha256:bc71c67a851aa1edcc590703bc01c231b841f03d178ce796d5d12fa8547c85f9`  
		Last Modified: Wed, 17 Sep 2025 21:10:13 GMT  
		Size: 2.6 MB (2598219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36e8fea722c47389c705d4a88ec0648992b71b22f11c652263321dde93dcb412`  
		Last Modified: Wed, 17 Sep 2025 21:10:15 GMT  
		Size: 14.8 KB (14779 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:07dbdaf2931286ed843faa7680be41247377829d5970fc25930cb2b9e49c806b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.5 MB (262511739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5fab96e75e916b2a56a38ea069e45e4167256d3310ffaae08f53351fd871af`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526072f9bf013cc544e774f4dbe054ff1f5fbaf55f176df5adc7181f772276a`  
		Last Modified: Thu, 02 Oct 2025 03:34:30 GMT  
		Size: 233.7 MB (233650164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:80e53158d4311d502f124a8ca0f45987d6b7fc65abc713d0174703ff95609b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2614023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd98dc6de440ce2887a9e78f282b13db87aef1238ed597503573eb193c4a3391`

```dockerfile
```

-	Layers:
	-	`sha256:8708dbcf08a96b3c1abbbbbc289fdb75ed68df5ab2cd00664acdf88cb98116e9`  
		Last Modified: Thu, 02 Oct 2025 03:10:04 GMT  
		Size: 2.6 MB (2598912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dcdc979db020382602c053f9797614b846f71c698c595ac9be04ee41f6608b3`  
		Last Modified: Thu, 02 Oct 2025 03:10:06 GMT  
		Size: 15.1 KB (15111 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:4ff765f20fd578b26d8f919406463ef88cf813aba017837dc58dfca79bb544b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.4 MB (271422842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7775612951297bb9d2a4f39300ed9702a62bac0a50a144d155edbd7eaf756e3f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2916723ef805077b21c00c74bd83d47da74ee190f326e7bab08e1a68cabb2f7`  
		Last Modified: Thu, 02 Oct 2025 04:11:02 GMT  
		Size: 237.1 MB (237119295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:14ff0ba63fe33c73061969f58eaae2971f17f447365c490b428ae1056cfb7e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2608763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c7c9b12de4724d3abba78f8826d6546f5c6cf77472f56c4c873170eaee514e`

```dockerfile
```

-	Layers:
	-	`sha256:18f42e4dc729e189cd7968acbe9a982817473f63aed60cab07f3bbcdd0394cd4`  
		Last Modified: Thu, 02 Oct 2025 06:10:20 GMT  
		Size: 2.6 MB (2593826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97d133a71c5706b3f330bc02bb8f0cc1da2f0f716ca94e51473c04f9b7a7fd0a`  
		Last Modified: Thu, 02 Oct 2025 06:10:20 GMT  
		Size: 14.9 KB (14937 bytes)  
		MIME: application/vnd.in-toto+json
