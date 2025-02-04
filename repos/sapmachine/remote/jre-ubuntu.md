## `sapmachine:jre-ubuntu`

```console
$ docker pull sapmachine@sha256:deb8983968a817bfe1f98f169599b00bfe75498d78eaeafc9dfce467a5ed92ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:3c47eccf314f42ba6a1c7071d17656357297e3700ab65fdebe3a37ee48976c53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89914076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09093353d3057374502f1dbe725686253323295009015ba22451822a94f97a6b`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jre=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:8292a23f8ab629ee8625a24ae99ac107102ec903b5a520f986f539a84f5b0dff`  
		Last Modified: Tue, 04 Feb 2025 04:48:18 GMT  
		Size: 60.2 MB (60159786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5902377b8cf57a85a6dfcc9008092d70ea00a260125491d32a88aaa27d748317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9db616a463ff352e82e2677b570099ba66de0d31972cf689c7d0122006426d`

```dockerfile
```

-	Layers:
	-	`sha256:159804195bf70afe862690bb4614801eaffe73f3ef2294307174f41cd5f6f098`  
		Last Modified: Tue, 04 Feb 2025 04:48:16 GMT  
		Size: 2.4 MB (2391257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcad235d53c4665a9836f5b6e553d5328d2860708819f32cefe9a5c2f8905f5e`  
		Last Modified: Tue, 04 Feb 2025 04:48:16 GMT  
		Size: 10.4 KB (10426 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:eb1d00a74d03eff3f0ad70dc0e5dc49fb5ac3022b228d820ba49ea20ddba0c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88132012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270abed34ae88af3aa77752336bed066da728696087519ec2ca91a86f52908da`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jre=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:855e6668894353ca8cbd7340e8397c91f158358831143577a3b427675ac47566`  
		Last Modified: Tue, 04 Feb 2025 15:19:28 GMT  
		Size: 59.2 MB (59238414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bd11c99757fa72117ed708e5931b0490b18adb34df51d060ed1ef29a963039b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8047ff0d020bff9a7ff7c627e26b9f57bd4028b5ba22ac49cac845409c597f`

```dockerfile
```

-	Layers:
	-	`sha256:6b941c19db64509f960211caef1d4789b6f80dcd048ecff83ba3fd65d19223bf`  
		Last Modified: Tue, 04 Feb 2025 15:19:27 GMT  
		Size: 2.4 MB (2391155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68dabc863fcfcd9fac884ea6019d892845430a1cd037d49ee6cecef978000108`  
		Last Modified: Tue, 04 Feb 2025 15:19:27 GMT  
		Size: 10.6 KB (10590 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:2260919857fc74fab574d99234115d59e8475f2a0dc1d93b0261f305d84740dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96113957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99cfeeba1ea48d305ffbbcf00ac7617ecda3bd44dd25fa3bb6162b9cf504bcdb`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jre=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:dd6ee7862d80df28a9fbaf94b667cbbc60238f8566daef52427747e02b28165e`  
		Last Modified: Tue, 04 Feb 2025 14:23:45 GMT  
		Size: 61.7 MB (61724133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7ed37295f04c7555cee15d6bf6f49d00eef50a0fa4305375a8a7af8c8ad7629b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2405096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2407cac68e61c59d190f7120c04afd0cd3479b7b2878f3566f58225ee6116656`

```dockerfile
```

-	Layers:
	-	`sha256:f946854f7bd697f8cfcc6401bda685360687aa4c86dab64ee9075b90dc37c364`  
		Last Modified: Tue, 04 Feb 2025 14:23:44 GMT  
		Size: 2.4 MB (2394596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f34a02b77a1413e0a95696f97c50e081ddfcc120c3da20e2cf23066a83ef11a8`  
		Last Modified: Tue, 04 Feb 2025 14:23:43 GMT  
		Size: 10.5 KB (10500 bytes)  
		MIME: application/vnd.in-toto+json
