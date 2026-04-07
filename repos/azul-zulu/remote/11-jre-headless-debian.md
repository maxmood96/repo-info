## `azul-zulu:11-jre-headless-debian`

```console
$ docker pull azul-zulu@sha256:7e63e4f2c12d52950c405ff0f021463d683f27c37a145b862897e7593ba50d88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-jre-headless-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:310fce648a714b17a79bfc5657a91cee1263da0e8244ef17a6a2656bcc0632fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94764175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12ced525eda10ebd712b4221f7cae10f4d5260a9c3b24b1f0336c63f500cd64`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:44:32 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:44:32 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:44:32 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.30-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:44:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6c952914e448652a4d3475cfb1b13d1fd4e5d75e8535cb56509b4ccf035772`  
		Last Modified: Tue, 07 Apr 2026 01:44:42 GMT  
		Size: 65.0 MB (64988535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:257ca4e4d019fe1a2dfd6ebe2c2b3cd444775d77e9a22b7c37948862eebcae99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db085b2d30a56230c295a989ecacb481e1d2c4a882dde1ed6535b42ab860419`

```dockerfile
```

-	Layers:
	-	`sha256:6c16dce19674cf232dadbf9b6d4386167c498d62c37bafb1dfeb1c7bf4f61067`  
		Last Modified: Tue, 07 Apr 2026 01:44:40 GMT  
		Size: 9.3 KB (9300 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-jre-headless-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:92811c4fe3c3eae75a43d3d405da7c83e8be5d913d04d2488c30b9eea119f2ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94926314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca32bf925b4b291850a739c7f5843b0457e8567ebdae852ec3f6f7c41553a12`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:47:39 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:47:39 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:47:39 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.30-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:47:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82cf584eca9c53836af262e804b50e0fff96468187895ee1f19810c19286523`  
		Last Modified: Tue, 07 Apr 2026 01:47:50 GMT  
		Size: 64.8 MB (64787763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:e357b840b3cb72df9901ee786a2473ed1b30c2f36463ebdd47e342eb9fcb56e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08440089f32d3f18ef86520e60bec2effabb04cd5c416b178b910ab93c104f9`

```dockerfile
```

-	Layers:
	-	`sha256:fcfc0409d4c10f7de884031e6b408d11f60ac3545aed609b77b6ffdd8c0c6d8d`  
		Last Modified: Tue, 07 Apr 2026 01:47:48 GMT  
		Size: 9.4 KB (9405 bytes)  
		MIME: application/vnd.in-toto+json
