## `azul-zulu:21-jdk-almalinux10`

```console
$ docker pull azul-zulu@sha256:c3e1feba03101f63f2809e27a2033acd408f64a02e2c09e1cc7bc513f523ba8f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-jdk-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:6da56556a73783d35f1c0418206f91dbc027dfb2babc3170fb2252df2c267ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233923518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47694e56998c02a2735be7fc89be2372088bc375403859112b6ec722162b4f20`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 26 May 2026 19:12:04 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 26 May 2026 19:12:04 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:18:25 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 26 May 2026 19:18:25 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:18:25 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu21-jdk-21.0.11-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 26 May 2026 19:18:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Tue, 26 May 2026 19:18:25 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:18:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e00696cab286036acbc1819dc14bffffe3d9b62859baec766357c34271aa510c`  
		Last Modified: Tue, 26 May 2026 19:12:20 GMT  
		Size: 68.5 MB (68456037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daad6bc98137a0432016eb014468eac38e6a8f9835b1068ee54b1543fe80e60b`  
		Last Modified: Tue, 26 May 2026 19:18:41 GMT  
		Size: 165.5 MB (165467481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jdk-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:c875a3d6cfa0cfc72b14007f6e0e58ad02410fa27d47cc946c31731e27527b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e536af79bd7bd5d96098390e5b811404993ab2a74c70f50fcc0d26cc4832bc1f`

```dockerfile
```

-	Layers:
	-	`sha256:4e6351fd9ad784f17841f5c60f06dfac6d195a7f59027490c4805884eb48879c`  
		Last Modified: Tue, 26 May 2026 19:18:38 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-jdk-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:af367f8c5765deab04761b87d601da31e02b832199010391175fe4b135c58f38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231755225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e814abbc94ffb990ef9f1d7e34f1c3a0ec3ba0eb4e16570b7a01906bc63d888c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 26 May 2026 19:15:08 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 26 May 2026 19:15:08 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:18:33 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 26 May 2026 19:18:33 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:18:33 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu21-jdk-21.0.11-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 26 May 2026 19:18:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Tue, 26 May 2026 19:18:33 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:18:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b1228b076bddc8d6b69c35f53b57866988d02e0877190f42b0390db4a24d6bba`  
		Last Modified: Tue, 26 May 2026 19:15:24 GMT  
		Size: 67.0 MB (66970892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef1fd5d0d2800c1ffcb3b7c4136387c08eed3e11d0d235e41f44d1f1479707d`  
		Last Modified: Tue, 26 May 2026 19:18:51 GMT  
		Size: 164.8 MB (164784333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jdk-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:275e31cfb4c39c566b38dd283fa3bd826275406d0df77acd6408dbcb9e96c8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d8085616e298c2f5699de5b31186f32fa18aa445c152a9089a7849d414cf3b`

```dockerfile
```

-	Layers:
	-	`sha256:f303016629409e0926e637973add14c8592a0bf4774f8928b91e73efa1c49b04`  
		Last Modified: Tue, 26 May 2026 19:18:47 GMT  
		Size: 9.6 KB (9586 bytes)  
		MIME: application/vnd.in-toto+json
