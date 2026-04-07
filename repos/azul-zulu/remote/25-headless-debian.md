## `azul-zulu:25-headless-debian`

```console
$ docker pull azul-zulu@sha256:526c574511156b19626951b509a56f13abbd9009de72d9d3b362a3ba3d04ef27
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-headless-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:f8054974813876ca293b3f4cf0a4940f20afa848886964698ce153c8bb509837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212384990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df3c20b06ee5608766f920ddeee20e035493c2831146a814c36857305661bd1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:46:19 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:46:19 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:46:19 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.2-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:46:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Tue, 07 Apr 2026 01:46:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7228e25ad8d6ee70257d57ef33700796bef21503ecd1f3ea8260d3eb1226ae`  
		Last Modified: Tue, 07 Apr 2026 01:46:37 GMT  
		Size: 182.6 MB (182609350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:cfc0527de7f5d167e911123b3f6d7ef40ecf9922bcf8a2ca55540026d967e26f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5473ae51ecd5f98277ff89d97781fd399381e022d4e744bfaf94c880bda1cdca`

```dockerfile
```

-	Layers:
	-	`sha256:873131261491dcf776789ad6e035f9da83e2aaaf1b16e426ce3f5221d0ad98ff`  
		Last Modified: Tue, 07 Apr 2026 01:46:33 GMT  
		Size: 9.3 KB (9295 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-headless-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:ecded61245f005b8bb73ec676a81e6b54fe8d7f3a976acab5e5046372b223d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.9 MB (211896202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b033e715a037de241ab1b62614aa27d1184861e7232f5cb405ed175580b3f7e2`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:49:25 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:49:25 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:49:25 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.2-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:49:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Tue, 07 Apr 2026 01:49:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da706449235a9573fdb3c023945a30e75d872c14b31608291b20024732b778`  
		Last Modified: Tue, 07 Apr 2026 01:49:45 GMT  
		Size: 181.8 MB (181757651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:8ed61206abbc7069e8234c52457c79d7d71fc9e2eca784b1e0b38199fe0efc80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:249d4ca9739812faab1edff3d51c15175a80151d5f636a8f4826cc2df6bc237b`

```dockerfile
```

-	Layers:
	-	`sha256:703a2c0f5c288c12f068b3f1cc158dd355d7894640128e87285d674ece9bfc38`  
		Last Modified: Tue, 07 Apr 2026 01:49:41 GMT  
		Size: 9.4 KB (9399 bytes)  
		MIME: application/vnd.in-toto+json
