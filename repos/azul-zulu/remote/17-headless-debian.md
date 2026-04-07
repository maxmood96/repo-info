## `azul-zulu:17-headless-debian`

```console
$ docker pull azul-zulu@sha256:14b05b922d349b07d43c1aee360c0e84e3fa669c264fdc6447c218e7e7d64ed5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-headless-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:922411813a8319a332d19accb1bd997520ca0f572804e82fb7c5963e0b4849b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.0 MB (180034300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba134b31c7bff0b294b3555efd22594d1d16e5096785738b303a04cb5e840b4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:44:57 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:44:57 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:44:57 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.18-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:44:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Tue, 07 Apr 2026 01:44:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f4a89607dcb52c9a0a9efbbc05d924b350103254640f9a5b26fdb0f45ac317`  
		Last Modified: Tue, 07 Apr 2026 01:45:12 GMT  
		Size: 150.3 MB (150258660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:d428b7ab47f3f51fb6722aea0b1641b7aa399f5ed43c08338b01736bd66bbab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60494926ca7d2beeeb7f80ed3f33bc53f3f5a9b785dbf7a980fd69376a53197`

```dockerfile
```

-	Layers:
	-	`sha256:fb29e5673d4d79e9543955622f6973cf24697e9a8bfdaf6c0bff90961ffdf060`  
		Last Modified: Tue, 07 Apr 2026 01:45:08 GMT  
		Size: 9.3 KB (9298 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-headless-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:b9f11d5a4c050e28286a0fe9c40840a2ff795bac411d8d257e6bde3ea7778af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.4 MB (180384145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f64985605b3a14ab398f6d132aa143e8f265dbe302bd32ef5da0da108f5a0b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:48:16 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:48:16 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:48:16 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.18-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:48:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Tue, 07 Apr 2026 01:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a461493e8b60eda8116b7c18ce4eea07989d94d7bbef606358845efcacdce5`  
		Last Modified: Tue, 07 Apr 2026 01:48:31 GMT  
		Size: 150.2 MB (150245594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:51864afbf9909f5b6f8dea37466987fe54a3f5bf369b57b234fc1e39435ae3ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6049ee8c21fe424ff052e8724ac9faff9f3c4a0f5f39392262cc07f48f74fa84`

```dockerfile
```

-	Layers:
	-	`sha256:e954de8da0ab2e2141ba7cca892a5d74ddd528dd246f2e2b2ca35a77d62a63a4`  
		Last Modified: Tue, 07 Apr 2026 01:48:28 GMT  
		Size: 9.4 KB (9402 bytes)  
		MIME: application/vnd.in-toto+json
