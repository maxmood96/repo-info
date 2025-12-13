## `sapmachine:lts-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:f23857ec439f66370b9a3677678b430e51a6e56eaa1a1e93ee46395dc034a022
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:a3627cc9c0e1fd2f3b466f43335cb85a7a25525b948a4b6617ec6758f2864555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86428428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaae1e0c290835d505629e633d61e0809836979dd61917adc1ba97f4831a8654`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:38:09 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:38:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 13 Nov 2025 23:38:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5739183329c0a85055af83440c95c450bd0a9a80176a624b807a6143da95a8`  
		Last Modified: Thu, 13 Nov 2025 23:38:30 GMT  
		Size: 56.9 MB (56891630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:06cf403e2e5b816ec89f8acd5def9ae580cff1aac74748457ef581d7372a8f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2561434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fcfa7c8f9b408b490bbe96c0ae67c7166e8d1ccb08d71f5d6768842e963f7ff`

```dockerfile
```

-	Layers:
	-	`sha256:4980227e7142f5715b0619bcf2c6ffa16e1d7a10d891a28db67df7031857a1b3`  
		Last Modified: Fri, 14 Nov 2025 01:13:45 GMT  
		Size: 2.6 MB (2551345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ff9a9ab7298085d253789a2ad578982eb4f6c635a34da3a5fad5230e549af88`  
		Last Modified: Fri, 14 Nov 2025 01:13:46 GMT  
		Size: 10.1 KB (10089 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:da584f978a8ff60eecc6d8d671336b3b9b61f1c049947c4aa107e4da01b847b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83163153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8284530169badd3eb0c09de97c6ada237125fb5efa3c98685215feedfd927dd6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:37:14 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 13 Nov 2025 23:37:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f66a02dd7938f6ffdc34d84bf267020c0facab07954564ea13779699c9b4fb`  
		Last Modified: Thu, 13 Nov 2025 23:37:39 GMT  
		Size: 55.8 MB (55779276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:95ab14918c1d86f1290fcda76043c8d6c2a904fd618aa454f2140d9906d7ae73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2561313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e79359cd954e1d951b5df89eabd59904a49f1bb24e31edb57a799b8c77a0c6`

```dockerfile
```

-	Layers:
	-	`sha256:d96e8a993a0472a44c2460885338cd0966f3c8851273b609c9b0da0bdb87b3b4`  
		Last Modified: Fri, 14 Nov 2025 01:13:50 GMT  
		Size: 2.6 MB (2551072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8b4976c542e644b335dd52d03069dbabf65d69284330444e72754999354f593`  
		Last Modified: Fri, 14 Nov 2025 01:13:51 GMT  
		Size: 10.2 KB (10241 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:49ae7bc95c49f2206a8ba7569ce4e620e74e5f47c37f7ae090347768c2283e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92134714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c22202ac227b8dca68f62b134a10d9f4d4ed9f1f2c08ce126072ed62b507434`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 01:22:14 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:22:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Fri, 14 Nov 2025 01:22:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Thu, 13 Nov 2025 23:02:18 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fb35869abc199f86ed1e0c780e31bb8399360af4f7df1e93af03cc734c71fa`  
		Last Modified: Fri, 14 Nov 2025 01:22:56 GMT  
		Size: 57.7 MB (57687992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5279815e7c202fc255e8e63807b4888e062b91d3610b659317f04a5ce8c9a2e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2559010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b6e19edff515377513bdb98e5815b72b23324f6344f313550fb014168c3748`

```dockerfile
```

-	Layers:
	-	`sha256:e37f3cbb9d1f10f101d3678bf5c4f3419d9ccedabe592b4a3648e79b7ee35bf9`  
		Last Modified: Fri, 14 Nov 2025 04:11:21 GMT  
		Size: 2.5 MB (2548854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06770b11b464a0c9900cefee9c420a60ef5aaa96f34ff27b8112358a3a365828`  
		Last Modified: Fri, 14 Nov 2025 04:11:22 GMT  
		Size: 10.2 KB (10156 bytes)  
		MIME: application/vnd.in-toto+json
