## `azul-zulu:8-jre-headless`

```console
$ docker pull azul-zulu@sha256:a8a9c36fa6e20d93daf412f26ec0d1c795bdd4a553bc6153946fb7ac6f37b9f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-jre-headless` - linux; amd64

```console
$ docker pull azul-zulu@sha256:dd4364c586dc9117189733723ff2809dcda9c7be55ef64481383b4c92e9f6a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77470936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f98c6cc561447de5de15835bc032be7701238cca84a04c26fbb5847ddbcffed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 22:11:21 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 17 Mar 2026 22:11:21 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:11:21 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.482-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 17 Mar 2026 22:11:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7cb9205ed70aba77adc70972644cde629967ccf46f08b90665f107c67249d6`  
		Last Modified: Tue, 17 Mar 2026 22:11:30 GMT  
		Size: 47.7 MB (47695436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:6866c0176b65c26c492f44e638393cfde0359ace67341fead3e51c3b64ab403f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4eecb92825586b16523bdbc9249e3f0d74b324debd05feafbb9cc403596c82`

```dockerfile
```

-	Layers:
	-	`sha256:9d614a03b025e7cbdb5d6bd6c538d057d80ae9fc3c837d693a0c6acc4b3eb020`  
		Last Modified: Tue, 17 Mar 2026 22:11:28 GMT  
		Size: 9.3 KB (9285 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-jre-headless` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:1c120c29b5caf30e9ba8aadd321e20cdbe053431720830317b1971e488e5e34e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77161605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164371aa7a693c31cd4f79274dc5fc8c4e56143b796d203eab35a230ec7642e5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 22:11:15 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 17 Mar 2026 22:11:15 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:11:15 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.482-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 17 Mar 2026 22:11:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d266f97aaf4f8c408b4f0394be592b8e2bcabc330ef3404e0c903ef286cb23ae`  
		Last Modified: Tue, 17 Mar 2026 22:11:23 GMT  
		Size: 47.0 MB (47023189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:ee0a70e0640aea2a680d4a958aab57f73d5fdd49403b7f6c423b091d2b845962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01a371baa3a707dad15f55dc2d7d1fb512061fd075f4872a612465dcb1e5d5c`

```dockerfile
```

-	Layers:
	-	`sha256:5473fbeb80488eb07b84ae38b328d55f5809e3d7c1437571688773c9393deaa5`  
		Last Modified: Tue, 17 Mar 2026 22:11:22 GMT  
		Size: 9.4 KB (9388 bytes)  
		MIME: application/vnd.in-toto+json
