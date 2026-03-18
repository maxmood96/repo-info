## `azul-zulu:11-jdk-debian13`

```console
$ docker pull azul-zulu@sha256:5d4c1b712ceead22edc51c14e389e24da68c0b6e3b4cdfda9fa4763d0e532016
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-jdk-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:05237b04b193956d5e4d6e025894c5478a525045feb98d99f375990a37dfc589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.3 MB (178265602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57baafdb27c9ae7b2d27bf92b1f60a8125c7ce494ff9bc7d671225dfc25aba7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 22:12:06 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 17 Mar 2026 22:12:06 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:12:06 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.30-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 17 Mar 2026 22:12:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Tue, 17 Mar 2026 22:12:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8160e4edffa2d22607f7442308bea57df3720ed7f2cf25193d89a015283917b`  
		Last Modified: Tue, 17 Mar 2026 22:12:21 GMT  
		Size: 148.5 MB (148490102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jdk-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:26d83412234c8630715721c19fc04bf331334ee2992681be6c373716a2a02aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79193336230fe5fb6cc796e4743a45ef31c06e788c7fe863dd6f5cf9c2ef292c`

```dockerfile
```

-	Layers:
	-	`sha256:8bf9371872761ff1f06239c623e010ba29e5444a4874396bf1048f4dac4fad77`  
		Last Modified: Tue, 17 Mar 2026 22:12:17 GMT  
		Size: 9.5 KB (9507 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-jdk-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:a6493507cdd0da02749a73e74c605a850a92560f775dee10eefdb8062e573f04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.2 MB (178232789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e842b23ea156aeaf3d98f06bf7372698dc944501d879b5ca19721237183a6f5`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 22:11:17 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 17 Mar 2026 22:11:17 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:11:17 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.30-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 17 Mar 2026 22:11:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Tue, 17 Mar 2026 22:11:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518f7dc6ff6ea312374ee37bdfd663935818f5601fef98460a5b3f2d18b83148`  
		Last Modified: Tue, 17 Mar 2026 22:11:33 GMT  
		Size: 148.1 MB (148094373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jdk-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:fa566d380e60e928dad72d38aa51bee7bc4978b57a22ea97624fc7b68e451c22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b72e03f2c03cf255fbea40dbdeffbd9f3abefd90952fedab772ac9890491a0f`

```dockerfile
```

-	Layers:
	-	`sha256:2c8865b7a6e9a6cfe978c06980ea05b1f023de6b60e42fcd63d39c60ba67dd39`  
		Last Modified: Tue, 17 Mar 2026 22:11:29 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.in-toto+json
