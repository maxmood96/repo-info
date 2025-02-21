## `sapmachine:jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:fe1360c34dfe08e18ea7e42efcd4fd69b039df8cc28370e13c8a41338d9740fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:d6fb17b7f262a333d0c466cadda608e1016c6196923a068e0b6536e9c82dce3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88729656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6210b465bdb02e7e507acacddacf81baedac036a16794a34191345808032b2d0`
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
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d515e61cce0af8ce59b8c5abfadb27fa41794f7650b676fb9e717bf9e880a5`  
		Last Modified: Tue, 04 Feb 2025 04:48:01 GMT  
		Size: 59.0 MB (58975366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:eb850de939c8aa053c855853a0c08805399d896a59e9873899fd330b00907e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d963516ad70f5b8d71f189f1e39ea85f4074b303ced06b6492d6c88f4b583e5b`

```dockerfile
```

-	Layers:
	-	`sha256:09dd827de280b26098aca17a25a1a1fe194e98287d3020789cb67431884e1f85`  
		Last Modified: Tue, 04 Feb 2025 04:48:01 GMT  
		Size: 2.2 MB (2154457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e737596fde1ef860fb68b83fb7cc1ab219b8471824c04f89ab8b60d99504f5c2`  
		Last Modified: Tue, 04 Feb 2025 04:48:00 GMT  
		Size: 10.6 KB (10626 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:8a7a7238e8482b5ecf72e8d8798c4e625ba5bb29204e8db9cd2e9f7cefee0d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86936818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d5a3eb20c2b1731ef9474618c9ea5478b4caa83460d78e3be6e9dac1b43dab`
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
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bccad08185f59721c7555f34434e1c08819d22a55e1bfea800ac1490eb8df07`  
		Last Modified: Tue, 04 Feb 2025 15:20:14 GMT  
		Size: 58.0 MB (58043220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4d4e21cb0ccbb89163471a19ed9600c0dabc50f67ec02ec2c50a7504230f3923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8be4426f9c4f7731cde6e496245281f29350c01651e98c7e024496289ff233d`

```dockerfile
```

-	Layers:
	-	`sha256:29fc4a746cfef80304463db4001e76ff5b5809452f63fbce1729dea750d7b031`  
		Last Modified: Tue, 04 Feb 2025 15:20:13 GMT  
		Size: 2.2 MB (2154346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:408936d01f30384cf27ccefd6584c926b9a36e693635bc1c17662753acaeaa85`  
		Last Modified: Tue, 04 Feb 2025 15:20:13 GMT  
		Size: 10.8 KB (10791 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:453dce80e3c14a771569f7c4a6f202a57d0ed0d2374bf650e2b207401badb365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94726832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f146ac73364357d9c6229e31c900f7f6bc98102102893cacab029fb503ccf3b8`
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
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9e448f8091aafe9a2899581500beb3c390937a192aebac0ad02756d7f10286`  
		Last Modified: Tue, 04 Feb 2025 14:25:02 GMT  
		Size: 60.3 MB (60337008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:23cc5b0a7518338a938798952d060edde35f264115fc1362355086151ce94e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2168434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829df587760818fac1caab0d5b474a504654fc1f6cc4853c437f6f9b3983c6dc`

```dockerfile
```

-	Layers:
	-	`sha256:8935b75e8e372d20ef6a7cc2cccd6ef2862feffe657b1f3ff9c8b0a5dcab0554`  
		Last Modified: Tue, 04 Feb 2025 14:25:00 GMT  
		Size: 2.2 MB (2157733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a69dea93f53edd94f51ffaa0dde3708e730711f8f8d5bc130f13233ff12b1812`  
		Last Modified: Tue, 04 Feb 2025 14:25:00 GMT  
		Size: 10.7 KB (10701 bytes)  
		MIME: application/vnd.in-toto+json
