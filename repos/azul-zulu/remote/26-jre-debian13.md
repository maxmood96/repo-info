## `azul-zulu:26-jre-debian13`

```console
$ docker pull azul-zulu@sha256:3177eee819fb52f4aaedabc3be8ce06be48b1453809eb16e11e81207c3ee5836
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-jre-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:f20b91335a850aeab84fbc8dd6537b65067507c43a5077d2151d6a581a5d1ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121838539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447e9e42e9cf5abd27356e414490863ab53fbe3eba2bc500704885b96898aad5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Fri, 20 Mar 2026 17:26:31 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 20 Mar 2026 17:26:31 GMT
ENV LANG=C.UTF-8
# Fri, 20 Mar 2026 17:26:31 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 20 Mar 2026 17:26:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce94d5783bade3a6ee7e4883d64a76e27cf5bfa0335f87e2b10c23ccd89dc65e`  
		Last Modified: Fri, 20 Mar 2026 17:26:45 GMT  
		Size: 92.1 MB (92063039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:928c187cb54699840b857264c5629503f031e1c057796dc16a08b9e1de029f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e539c22e78cb99e5f0cee64b8e44a7784090a2a6342486874a3d5ea984cc80cf`

```dockerfile
```

-	Layers:
	-	`sha256:98c28ec2a11fd9db122e0ebe18093a4c15348bc7f86860573f59a9e25a3cc428`  
		Last Modified: Fri, 20 Mar 2026 17:26:43 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-jre-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:7898eb61fc8b505e74ca2309e8d6ff10f13ffcb77a34d8dc016aad1c76e1ca3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.1 MB (122109998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03fce94944e872fa0d20cb946a83bc9fa88822282e626e4e47542e1e40d557d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Fri, 20 Mar 2026 17:26:43 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 20 Mar 2026 17:26:43 GMT
ENV LANG=C.UTF-8
# Fri, 20 Mar 2026 17:26:43 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 20 Mar 2026 17:26:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48564ec6d9bcfb7fea0132569c89c96f75a881363006baaec0a9c20f20182a19`  
		Last Modified: Fri, 20 Mar 2026 17:26:58 GMT  
		Size: 92.0 MB (91971582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:c200be25afe20bdc58880438bdebb557e1fdfd3a3e3627d230c24589926535ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05ca97b08ba3878bfada84eef96dcd15e8a9741b213f050cc62780becfabc43`

```dockerfile
```

-	Layers:
	-	`sha256:07a1ea6fadc31cba6e8d02e8a4918a35e6bf900c584b32714ce14ee09d4f5efb`  
		Last Modified: Fri, 20 Mar 2026 17:26:55 GMT  
		Size: 9.3 KB (9283 bytes)  
		MIME: application/vnd.in-toto+json
