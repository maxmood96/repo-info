## `sapmachine:11-jdk-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:90bd561a16d85288b03414b8c5d13ddebb8432219efc9ceb6e5e88f04880f7b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jdk-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:9edcb317c81a69647ca8973d522ae350795c79d4d70770aade5fb34c322abcfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 MB (230360870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd21b929de40161bc2c5589562a129152832064e7b707268cbc94a8c034d2001`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:25 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.29 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 21 Oct 2025 21:30:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870835ff9d4cf795949d5f1d0d41db297c04e151f4825b34f37d0513c8b4362e`  
		Last Modified: Wed, 22 Oct 2025 05:47:20 GMT  
		Size: 200.6 MB (200637723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:27fd9251e24ea6a51ea045baa386a9bc485c6fbb305064a7b8c875097daa5eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb8ad4f43b53a33a8623948ef429d21d9d745fe7822f1013f417cea9898595d`

```dockerfile
```

-	Layers:
	-	`sha256:9ed85ff4a65ae0c4b35d8b8fbe7e84e65a7dbf99a8b86ec2bf03ed98044bb1ca`  
		Last Modified: Wed, 22 Oct 2025 06:04:19 GMT  
		Size: 2.6 MB (2615590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27a4a785ec45e2a0c76f4329b1e192259a2fe1d161f8c823f3106f98a5782998`  
		Last Modified: Wed, 22 Oct 2025 06:04:20 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json
