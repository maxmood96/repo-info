## `sapmachine:jdk-ubuntu`

```console
$ docker pull sapmachine@sha256:e0d39ad5b438a0a05c4a4bb67c7fbcb424dabaaf929fdceca75a45d161b6c67a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:a4d74b70ca3bba00a1ad7e46706af525a591779d7da01ae329e4c5974b514aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245771580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2d7971024c5849afdb7e1451fd1634cbff49a73d0a78b214d02184d47eee56`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a45005dbcfff9284ebd035cf1c77b246cb1ea07d6c928b2cf18a1e6039347f3`  
		Last Modified: Tue, 17 Sep 2024 01:00:58 GMT  
		Size: 216.0 MB (216021752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:43a4c6f7480b5c8db03383f6ecd14c53fb357f7c2d12f6abc23a7641d76ae198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c4a30d902c2863a5531d6d826eceaeefe38da662f9da63ec22c20a640a44fc`

```dockerfile
```

-	Layers:
	-	`sha256:c37bd15168e15e890be673e99e64ac2f3c8997be259d1954f0c1035e312f44bd`  
		Last Modified: Tue, 17 Sep 2024 01:00:55 GMT  
		Size: 2.5 MB (2452748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4da4031b3a56985051bffbdcc190eaa9f7b0b710da967af2b2306bfb1a065d6`  
		Last Modified: Tue, 17 Sep 2024 01:00:55 GMT  
		Size: 13.0 KB (13031 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c828f15a00f4fe62004555b1174054ec0cdcd463b2b9d5b77e8443e9ec8771f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.7 MB (242710223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf644133370a8967cfc235b2defa04b481789ee28fcc07556141cc9a080afd0`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d624f0fd8ee771a9541ac21594f9bbe313fe69866d63f54acdd68c61235bfe2`  
		Last Modified: Tue, 17 Sep 2024 03:08:52 GMT  
		Size: 213.8 MB (213824624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5844048f4939346edce66141f8dbdf49915ded253b1e5cb857c80baf31568baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a67194882ae0908a804cd4e89d9faff7ca6ac305ac58b384a5e49be81fd7f0b`

```dockerfile
```

-	Layers:
	-	`sha256:bed8ee8261ddb2ff5d6a477a1775aa8a88ff13d8207f67f075376bad1e7c1936`  
		Last Modified: Tue, 17 Sep 2024 03:08:47 GMT  
		Size: 2.5 MB (2452752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4acd33a22a9826e5c316cda9a29f4112bc547e2093c9e55fa83fd3939396cd5`  
		Last Modified: Tue, 17 Sep 2024 03:08:46 GMT  
		Size: 13.5 KB (13499 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:8d9e77450c65ba9b28583c26fd7d1da93eff3299ab63d5d362f91ba651632683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.8 MB (251843821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfa7755cfb03be9e35ef72543f1f3653698dd054eada92012bbd49fc6ff3de3`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c526398e5e771684dae49961d5a74cd9606dcbcf7ddafb1fcc1433293927dca4`  
		Last Modified: Tue, 27 Aug 2024 17:08:24 GMT  
		Size: 34.4 MB (34392345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebe2bc7f57199ecd3d14c73dc79db0c9fa8233cc155ea1dad2504d80130aa85`  
		Last Modified: Tue, 17 Sep 2024 02:16:53 GMT  
		Size: 217.5 MB (217451476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:26bb5130d42d103c314d3f078ebee9a2ade067250fc9ebb4ce9997224a36eb4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f03b4b46ae2b5c93303363a1079de8ea799321bfa4e88c41d602d0b4bc16a7`

```dockerfile
```

-	Layers:
	-	`sha256:6d388e04acb68774c140ba0b3aa92f78e7ec73457d78e52a925b7d6291a14f0b`  
		Last Modified: Tue, 17 Sep 2024 02:16:48 GMT  
		Size: 2.5 MB (2454201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a54bc3026ce9520607af1b5e4fcc43e526c1c418138b69c35d4a9a1df19d867e`  
		Last Modified: Tue, 17 Sep 2024 02:16:47 GMT  
		Size: 13.2 KB (13152 bytes)  
		MIME: application/vnd.in-toto+json
