## `azul-zulu:25-jre-debian`

```console
$ docker pull azul-zulu@sha256:da0c8479f1efe01e13580a5014a265774b41595951dc65984b6cac849c854977
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-jre-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:9f0f5aa98f4ce79e5aa645329f31f5ef8a93e9c4f64e183482a6cd72d1d85726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120829235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da98c3886286792c604bce58e62d41a707a1268ae3cadb08db22e17bd00d02b8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:39:30 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:39:30 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:39:30 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.3-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:39:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4846048dfc99d9350bcd03dcefe3d13465f8c15d1647585c0486a549b97776e`  
		Last Modified: Fri, 08 May 2026 19:39:44 GMT  
		Size: 91.0 MB (91049009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jre-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:87052c37443c7d03fcf27cc16031e8efb169aa80366f00803621928340e1c50b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c3f91dd238d22830ea32d74c6a2229da6dbf2c653c908a24e989684f031579`

```dockerfile
```

-	Layers:
	-	`sha256:4efa1134014163bb00062c6ee6aa7f56df4e889c55fafecc0000017e2a95dc4f`  
		Last Modified: Fri, 08 May 2026 19:39:41 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-jre-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:3b7c5172680995d93ef96a9f85a728673c98b0895d99568c831abd9c17e6d1b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120778635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9e56565bbfef680f066daf4cd706aac9413844d7e9cb8e6e9f7687eb814bcb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:41:48 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:41:48 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:41:48 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.3-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:41:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884765915c0161f938b4e73b2ffbf337a12404839a32163041d1f5ccc672420c`  
		Last Modified: Fri, 08 May 2026 19:42:02 GMT  
		Size: 90.6 MB (90634993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jre-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:6573b93279d4b6edefa4ceafffc9640fc89fce3beeeb18889cc1882c4906359e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3163b9972280058998e6003b37fbae55280d2b8f3c3b323a6b92cd5a2e49ee5b`

```dockerfile
```

-	Layers:
	-	`sha256:5cb3d369f0270fab54bbb4f820d08d44ec20856bfd1bf7b2e209bcd65ab8a552`  
		Last Modified: Fri, 08 May 2026 19:41:59 GMT  
		Size: 9.3 KB (9291 bytes)  
		MIME: application/vnd.in-toto+json
