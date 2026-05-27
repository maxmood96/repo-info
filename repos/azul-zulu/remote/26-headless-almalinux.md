## `azul-zulu:26-headless-almalinux`

```console
$ docker pull azul-zulu@sha256:01ba5968265fb1fc469560c268e3429336d38d7198c50e41280fb5661a1f81b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-headless-almalinux` - linux; amd64

```console
$ docker pull azul-zulu@sha256:22fa6d0ea9575cc4dc0e6a754b63bcb42967ef29533de02f8ac17652654b5e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254706199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c687c04b510b6edd02ba877b294be4648b6a256658f413abbbc738a686a93fdc`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 27 May 2026 00:13:12 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:12 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:19:55 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:19:55 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:19:55 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu26-jdk-headless-26.0.1-1;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:19:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Wed, 27 May 2026 00:19:55 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:19:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d656c7137a90f7ddb91de182a69468cac7f42400a3d603e1dc41b15db6101bd5`  
		Last Modified: Wed, 27 May 2026 00:13:28 GMT  
		Size: 68.6 MB (68560313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68fbaf640904778c4b878db48bfa2ca8dc6124dd0cdf993806b28f28acfa3a5`  
		Last Modified: Wed, 27 May 2026 00:20:13 GMT  
		Size: 186.1 MB (186145886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-headless-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:0639ae0b63075a04ae496a2001dbcf97229ae3a7fca5d0e533923058a8b81030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4b49be2244cab6c9d709daf25c921461590c701fbf01b92d6350c7c42b6bdb`

```dockerfile
```

-	Layers:
	-	`sha256:726c76f4a7eadd63a5c0aa7c3a4fb0549c437a1ea14d3d954d9ab36debbff713`  
		Last Modified: Wed, 27 May 2026 00:20:09 GMT  
		Size: 9.2 KB (9232 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-headless-almalinux` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:5283ad62e98dd63f9e3518cac4f77c44fb97cbd9fb8ccb745034dafceee24727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252972855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6720dee67c1d01782a47505145d79b13deaba848eedc9066299a9bd4e0bc17af`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 27 May 2026 00:13:34 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:34 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:19:17 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:19:17 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:19:17 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu26-jdk-headless-26.0.1-1;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:19:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Wed, 27 May 2026 00:19:17 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:19:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2e6581d4e57d2c64e98e26766f719408796b49ab923bb5ba71515cd98debeafe`  
		Last Modified: Wed, 27 May 2026 00:13:50 GMT  
		Size: 67.1 MB (67131734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645f4156893949c0c4f5f13ca3d2116c6a29fc803912e95499a8cfc21dd2ec3e`  
		Last Modified: Wed, 27 May 2026 00:19:39 GMT  
		Size: 185.8 MB (185841121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-headless-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:9b9643afbc2ff05b786bf0a384d463c160af13fe2e063eb79a5062e48c285a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c938cf95a334e881cd9a4aee18302059ec12d4f9a2a1e3edf15f5fd0ca999155`

```dockerfile
```

-	Layers:
	-	`sha256:5674ab760ad8f1e6cd34d9201cf608078956629b7a51eaef0be51971564788d1`  
		Last Modified: Wed, 27 May 2026 00:19:33 GMT  
		Size: 9.3 KB (9323 bytes)  
		MIME: application/vnd.in-toto+json
