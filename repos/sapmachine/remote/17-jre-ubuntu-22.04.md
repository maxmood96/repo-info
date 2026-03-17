## `sapmachine:17-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:9720573bf27bab3bea6c3f019dcb7fc88e903bdbc507520fe9ffb3c0d0927c7b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:777f1a99358c433e66900c2bd71e96375c67b0a71ae8c477745fc3555056b921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83921256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747570cb613d5d41add5661341ddad3f10dcb37fe90378bbd8d07f0d0b20f1eb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:25:40 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Mar 2026 02:25:40 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabb30c4ed6944f11b85e7bd9f592587da776133d30a15328d644f8c54e2a0fc`  
		Last Modified: Tue, 17 Mar 2026 02:25:52 GMT  
		Size: 54.4 MB (54382736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:260d55c3ad73a4f2c8a96a6fb626f51552c18236445952f585865d05ada1fae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cdedfbbac596fd8a6d4601b707e17867383459c2ae67fa9003761fdac42b795`

```dockerfile
```

-	Layers:
	-	`sha256:6d36f9bf1857b1102d499973f58521c6282f8d67849b996c8823fe7359010cc3`  
		Last Modified: Tue, 17 Mar 2026 02:25:50 GMT  
		Size: 2.5 MB (2546027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f66fd42977080b0190eddc690b8bfbe5fca6a73c98cf47d50f4fe1187183f81c`  
		Last Modified: Tue, 17 Mar 2026 02:25:50 GMT  
		Size: 8.8 KB (8774 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c2daa347b0f10ee7b07ae4afb6c9ad5cc6e009080e19ec987c0f9a5a5a501435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81159207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6809c24d8685f8a1cd96c3f9bbf14900aa18ee4774ccdc0603097a8ee855e45a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:31:45 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:31:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Mar 2026 02:31:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12f28e4d52e4dea7349810efb360585ee70bf57aebdff8719b2c5c05038199e`  
		Last Modified: Tue, 17 Mar 2026 02:31:58 GMT  
		Size: 53.8 MB (53770182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a2ce8cb2c826c75ce2f7604357fd051adcd6d1899bc302325c71ed2e75357cff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e845f540754a20baeb5998361d50c179489f88fe64b6035c7738536b434c83b1`

```dockerfile
```

-	Layers:
	-	`sha256:ad14508bb9f611b530e22a441520ae03f9070e47b5cb9770c694f3b3686ed54c`  
		Last Modified: Tue, 17 Mar 2026 02:31:56 GMT  
		Size: 2.5 MB (2545709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21675c94778971511d7fa5e5dd286bed903c14b3c830ea3d77b8bf85b5ae47ce`  
		Last Modified: Tue, 17 Mar 2026 02:31:56 GMT  
		Size: 8.9 KB (8878 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a696c2a5d02c5ef8d57520209fae12d2b099d595ce2a8c4c1ffe3b6f14af14b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90011986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3094379166f334085cb3e8e854051e67ff3ac484a4a0e0f93fa5669ce7870e7b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:41:33 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:41:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:41:39 GMT
ADD file:0418bf4995f9b54380cc1e509e3f7d65bb07aed9a367528d0b1084f0a34f3bf3 in / 
# Tue, 10 Feb 2026 17:41:39 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 21:41:12 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:41:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Feb 2026 21:41:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:95401e425d899946469007a0ce4b02622cf84a67cdd684aa25d61d472fffc38f`  
		Last Modified: Tue, 10 Feb 2026 18:13:52 GMT  
		Size: 34.4 MB (34446102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c881ef8c90b95709e0e76f12110e063e0ca8922562fe3085cf8d38bcb1f56f2a`  
		Last Modified: Tue, 17 Feb 2026 21:41:53 GMT  
		Size: 55.6 MB (55565884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:087c4445166a40794da04e9e7c671094161940409a823962d740fede30ec2473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd61d32fe15907e466df48ab8cbeb4bb1e0a5b3fd29230e0b8e1dcf5ca177d8d`

```dockerfile
```

-	Layers:
	-	`sha256:5539c019e712dcf7627e159e3348ffe3101c43c71b1c7b3534c58af42a46052e`  
		Last Modified: Tue, 17 Feb 2026 21:41:47 GMT  
		Size: 2.5 MB (2545559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9c94eef4e2dff4e53388b7614a1208f83cdc8d9b8f4a03bead1c4b14a2e56c8`  
		Last Modified: Tue, 17 Feb 2026 21:41:46 GMT  
		Size: 8.8 KB (8818 bytes)  
		MIME: application/vnd.in-toto+json
