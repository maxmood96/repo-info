## `sapmachine:11-jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:68d1b9a223d712c4674803afdaca5eae828da072d1051e4a24e4a1df882ae1ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:d1bc85089dd6b0726eaff9f5bd019bc4aee172445c81bf9278a7b52156d22acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78934772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b118ed2da41c755110d9d8ab50de667a9a57191d127807a10fd9fb3dca00b93e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:16 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:16 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:16 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 15 Jul 2025 19:58:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.28 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 15 Jul 2025 19:58:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad12d5ad5a1290bc2b1ce5beabe73697163d252fb23cbf57ac5c13ae35f0fee4`  
		Last Modified: Mon, 15 Sep 2025 22:28:41 GMT  
		Size: 49.2 MB (49211322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4d50a840123934a1680093129379080a9b9fd3805ec6a9e9e92aa0cb4e4ad1f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2288087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1670e01104ee9204ab6f7c427ae44e9483c3fbb9fcde4bef0b1376eb6ea12e`

```dockerfile
```

-	Layers:
	-	`sha256:82c772918063386160ab331d64c6a30eee535da85eeee4edd31982a3b3a9438f`  
		Last Modified: Tue, 16 Sep 2025 00:04:42 GMT  
		Size: 2.3 MB (2277811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24c608d20988cbf95bf9c0f071cf54165533e1a0a617363a053f6e507776c4d4`  
		Last Modified: Tue, 16 Sep 2025 00:04:43 GMT  
		Size: 10.3 KB (10276 bytes)  
		MIME: application/vnd.in-toto+json
