## `azul-zulu:17-jre-headless-debian13`

```console
$ docker pull azul-zulu@sha256:1c7e2e08a93169907a4111bbcad31696b82aaa6060a66d0b03ec63244b8523eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-jre-headless-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:a9d7d4162b6a0a598a518148f8fccd7216a6f369771c2939cc8ba966cf4b663c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.3 MB (99308975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5affc674312089747587d6fe7cd398ecda5c7dd4e79b04b4cb8ce0c8edde2d7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:20:41 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:20:41 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:20:41 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:20:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455b09c1396f5a7ff1f841efa87ebb4ed978aa605808735e9182b0cb8d2a3f1d`  
		Last Modified: Tue, 19 May 2026 23:20:53 GMT  
		Size: 69.5 MB (69529049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-headless-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:c602e71d326b3569153d8e79f755d9441893250394e52d8de18079952a5782d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b46cac775440e748ac4ff5b859813a05760ef83df8423a1c058882bb9e9f67a`

```dockerfile
```

-	Layers:
	-	`sha256:abf756d969d511f7f18f656d3db4734a61c90d223f45beed08528769e725aa65`  
		Last Modified: Tue, 19 May 2026 23:20:51 GMT  
		Size: 9.3 KB (9301 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-jre-headless-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:476646c3d447babaebbabbb840c97c672659284bf6fe06fe469106fbce304f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.7 MB (99726424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba829ff10ca833ab286cb687b6ff094656689f665975b5ea845fbee5e13d2d67`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:02:29 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 00:02:29 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 00:02:29 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 20 May 2026 00:02:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508d900abe1218c2f2bec8c2d42b85552e7b79aebf1391f93b5b1156446a20f1`  
		Last Modified: Wed, 20 May 2026 00:02:42 GMT  
		Size: 69.6 MB (69584505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-headless-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:f755d8b9478e971de1d047dd0ca608f7833f9e0983448622d9c73e04a79d9070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45299f6391e5e1f7f4c65d074698e217188bfbaf1d459a88d15fa2a95817c68d`

```dockerfile
```

-	Layers:
	-	`sha256:867667adf888f7b5257cd2573f0bf82d2fd3b4c6040a0655cb6251b8cade5aaa`  
		Last Modified: Wed, 20 May 2026 00:02:39 GMT  
		Size: 9.4 KB (9405 bytes)  
		MIME: application/vnd.in-toto+json
