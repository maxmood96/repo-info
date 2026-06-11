## `azul-zulu:11-jre`

```console
$ docker pull azul-zulu@sha256:91f49e136c7a225f7fef5c19534b3279d06c0728a1a83dcd796a07507f47606d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-jre` - linux; amd64

```console
$ docker pull azul-zulu@sha256:3e5ce5c3032b366cada0a4c448e3f4a921b4938016bf82ecfa536e67fdaef527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96904101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:962276942a37e31b2e386d80cf3ea1e2d77e17f779d080610597024a88fa8d0f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:39:07 GMT
ARG REPO_HOST=repos.azul.com
# Thu, 11 Jun 2026 00:39:07 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:39:07 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Thu, 11 Jun 2026 00:39:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4b42ee6d8db701b28fa59ebddbe19fe9fb31eef4cd8b0da3d2230c0dd41dd2`  
		Last Modified: Thu, 11 Jun 2026 00:39:18 GMT  
		Size: 67.1 MB (67118686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:652720a449d263e2af9f2e43c3c79fb49a1d91cd5ca72c8d236938a1dd0ef7fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9ba447dd8b2ede4f70ae4596a143b7f70a17dbe066040d60cd77c8c45b41ae4`

```dockerfile
```

-	Layers:
	-	`sha256:188b5c274deda53d6083b5375ff2d28288fb0c36dee8fcf4e8f8c8982c0f0b0f`  
		Last Modified: Thu, 11 Jun 2026 00:39:16 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-jre` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:f05cbde0a4f2d8dc3000f741660216f14c436d1ed377d6e678bd4764a206bdb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97073260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501bcd406238a1e422e0d57aaa3e1cb70dc2bdcd04c4497f2ec4242e327e57e4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:40:41 GMT
ARG REPO_HOST=repos.azul.com
# Thu, 11 Jun 2026 00:40:41 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:40:41 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Thu, 11 Jun 2026 00:40:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bc0c2787d0191877eea863b6bd84336640b71f29d76e10b3c721219304b05e`  
		Last Modified: Thu, 11 Jun 2026 00:40:52 GMT  
		Size: 66.9 MB (66924730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:a10103aba49efaa39aaa61ac51d0ec129e1edc650c5d8891676abd70b1f98630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c35074fff4445eaff5894ea00682bea6dad84857d50168fbb6414449484ec57`

```dockerfile
```

-	Layers:
	-	`sha256:380f1523acaaac607c54a5c35e85bb832ee2d563e77baf916205bbe19a4d891b`  
		Last Modified: Thu, 11 Jun 2026 00:40:50 GMT  
		Size: 9.3 KB (9294 bytes)  
		MIME: application/vnd.in-toto+json
