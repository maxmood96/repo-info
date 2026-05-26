## `azul-zulu:17-jdk-almalinux10`

```console
$ docker pull azul-zulu@sha256:b43f070dcbd9df53960220a49b3cfa8563e369b5df19f3dfeebe4f122ef250f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-jdk-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:0370cdb38f8f50312383a9110f25cea4c362fe584d332bd2252e31bfc99b4c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 MB (220627475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5beff8e7a694ef38c556bf888b78722a52b0b5f39c32320f1ebd2aca27d92ccb`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 26 May 2026 19:12:04 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 26 May 2026 19:12:04 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:18:08 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 26 May 2026 19:18:08 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:18:08 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu17-jdk-17.0.19-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 26 May 2026 19:18:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Tue, 26 May 2026 19:18:08 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:18:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e00696cab286036acbc1819dc14bffffe3d9b62859baec766357c34271aa510c`  
		Last Modified: Tue, 26 May 2026 19:12:20 GMT  
		Size: 68.5 MB (68456037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5430948cbd36ccd0c16a6eaba0c819c5897f744f478851ffb0e4f1f9ad45213d`  
		Last Modified: Tue, 26 May 2026 19:18:23 GMT  
		Size: 152.2 MB (152171438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jdk-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:7fc18ded8aaf5939c0a9b42daa6698b866a5fddac661eb84d8fd65699815c367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca33db48cb59a7015c6b7323445f4c0ada79723a5f62489943174f65df5dbe5`

```dockerfile
```

-	Layers:
	-	`sha256:eb1fd71bd048f3a80d1ed917c2eebd315a6370e01b1bace81209cdc66dc37573`  
		Last Modified: Tue, 26 May 2026 19:18:20 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-jdk-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:37addafca5ba30662d02475031d6574b6f36eee3a72b55fc4e523984b979d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 MB (219167450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8001594d37a0c74decdd43cd5ad4269f6bb628beb7070f4a6e7f1444477146`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 26 May 2026 19:15:08 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 26 May 2026 19:15:08 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:18:12 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 26 May 2026 19:18:12 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:18:12 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu17-jdk-17.0.19-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 26 May 2026 19:18:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Tue, 26 May 2026 19:18:12 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:18:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b1228b076bddc8d6b69c35f53b57866988d02e0877190f42b0390db4a24d6bba`  
		Last Modified: Tue, 26 May 2026 19:15:24 GMT  
		Size: 67.0 MB (66970892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dbe9f7cea503512c284a141bf715ca0944ae3b8f3202c2ad32ba0c0f7c8781`  
		Last Modified: Tue, 26 May 2026 19:18:27 GMT  
		Size: 152.2 MB (152196558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jdk-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:6411aeda5db04fe92ca4812a2895ec8b2722ae5ba7760c896ac7e9befdc3a507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b8eefdf6ed5aaa4ac41e0491750e0b94afee10b209bacaabc8e5b66c68352e`

```dockerfile
```

-	Layers:
	-	`sha256:aeb1371e0005c6d50edc50e820bdb882beacf40d8e337b42a784d891b3fe96ae`  
		Last Modified: Tue, 26 May 2026 19:18:24 GMT  
		Size: 9.6 KB (9585 bytes)  
		MIME: application/vnd.in-toto+json
