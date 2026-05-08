## `azul-zulu:25-jre-headless-debian`

```console
$ docker pull azul-zulu@sha256:641caf292d69950e351613eaa63c31db4d4dba8df2f50b929e9345ce2b5e1009
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-jre-headless-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:3cab68e29b6199df1b11c967ede8934d8edf00c1e0d61375d782194edc2c6e07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118768694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edcdf7e0b8728fbf2c2f729b3dd21cdffcb03c5ab58a60fa26181ee4db7ad0c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:39:38 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:39:38 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:39:38 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.3-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:39:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2b0c2da5119d7efcac53124a9ab68b88e12c8dfb95914a83e1cd594fef166f`  
		Last Modified: Fri, 08 May 2026 19:39:52 GMT  
		Size: 89.0 MB (88988468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jre-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:76ddaebe8eebc03055e98eec969e0807554c9139d73b309f6529c3591c080c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d572c69cf53d0071ff22ef7ed015cac4441a41f8a9079bfc91fc1c13f73cfe7b`

```dockerfile
```

-	Layers:
	-	`sha256:5bcbdc6ccee5fa56bc0467270601190656cc0c9154c83d281eee240c6f478d96`  
		Last Modified: Fri, 08 May 2026 19:39:50 GMT  
		Size: 9.3 KB (9298 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-jre-headless-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:8498ac0e0a07e44bb44b3db0a2809193ee6911197467c2cdbe59bb491172f8d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118740143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b2aa876b6d2e638bda202e9acf30c771f1421b87b9e9f89ecd63e6a89f2134`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:41:50 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:41:50 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:41:50 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.3-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:41:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632d80803c82a493e7c95b48af55f48bf904514d5658c8db95b2e016fbb16024`  
		Last Modified: Fri, 08 May 2026 19:42:04 GMT  
		Size: 88.6 MB (88596501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jre-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:5c4dd1e1f58bd9e75e307749b0cd3ecf2303d52b5fe3695ba070485e7e9574ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ce5ac36b0894f83490aae3b9f4847d756d63ddd4666fd28eef3a405f51afe7`

```dockerfile
```

-	Layers:
	-	`sha256:e798a561983f12c53c4bfda6462204a85c2c5f566fd68f63e1f09ebe22fcac4b`  
		Last Modified: Fri, 08 May 2026 19:42:02 GMT  
		Size: 9.4 KB (9402 bytes)  
		MIME: application/vnd.in-toto+json
