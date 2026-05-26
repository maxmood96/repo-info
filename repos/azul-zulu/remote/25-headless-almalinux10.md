## `azul-zulu:25-headless-almalinux10`

```console
$ docker pull azul-zulu@sha256:c4c83d350982f0989eb01ae67fe4ee2f44e2befb225715692271a416e8b76cd4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-headless-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:08ead374b52c4e91f8656fe166ce8f7a5b7980d173bbd8883e446a320d26d90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.3 MB (252315759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ffb8551755116a4e38fe33ced576cf69dffbc6e52e476d628b8e4484f9d58e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 26 May 2026 19:12:04 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 26 May 2026 19:12:04 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:18:29 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 26 May 2026 19:18:29 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:18:29 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu25-jdk-headless-25.0.3-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 26 May 2026 19:18:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Tue, 26 May 2026 19:18:29 GMT
ENV PATH=/usr/lib/jvm/zulu25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:18:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e00696cab286036acbc1819dc14bffffe3d9b62859baec766357c34271aa510c`  
		Last Modified: Tue, 26 May 2026 19:12:20 GMT  
		Size: 68.5 MB (68456037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7006d6010f74d776f289a146353bb71a6453f8b6197b0f27da3fbaea68e4d046`  
		Last Modified: Tue, 26 May 2026 19:18:46 GMT  
		Size: 183.9 MB (183859722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:7948f48d6fd8ef7d4669d58a5080e14d7b2f6a78cdf6cb2d55acb4854b68c65c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae2a86ce525df7c2428098f7ca49a712efc3a63a9cd28c2bb6f3737595674f7a`

```dockerfile
```

-	Layers:
	-	`sha256:09d4fe8fdcdb904a9cf43f021c8d9f9eceb849d8ba45bd8466c93f99e0820b9c`  
		Last Modified: Tue, 26 May 2026 19:18:42 GMT  
		Size: 9.2 KB (9231 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-headless-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:90d35f7513c9591e551ddf16c4d1c7b51c5833d9bb7e6b91f1583a1f1015d78f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.0 MB (249980873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45670b15fcd8a6385d60147dd8c266485e3e29c0559651b13ed7907f034b2196`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 26 May 2026 19:15:08 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 26 May 2026 19:15:08 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:18:42 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 26 May 2026 19:18:42 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:18:42 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu25-jdk-headless-25.0.3-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 26 May 2026 19:18:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Tue, 26 May 2026 19:18:42 GMT
ENV PATH=/usr/lib/jvm/zulu25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:18:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b1228b076bddc8d6b69c35f53b57866988d02e0877190f42b0390db4a24d6bba`  
		Last Modified: Tue, 26 May 2026 19:15:24 GMT  
		Size: 67.0 MB (66970892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed641d7a25e546f0744321d1efa62fcbee1dce6fd1734af6f4d486497caaed0`  
		Last Modified: Tue, 26 May 2026 19:19:02 GMT  
		Size: 183.0 MB (183009981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:33619f22caa5dc49239e422a58ee645ca65102d1a70a096364b177e330f39d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ddb3c3cf11f0b5de4eb1ea094b673d232cdaf2f8bfd688fd088a35836f5a50`

```dockerfile
```

-	Layers:
	-	`sha256:743061c4e542bf706330b159d044d793955a614b0912400a7c14bd9f531d1f8e`  
		Last Modified: Tue, 26 May 2026 19:18:58 GMT  
		Size: 9.3 KB (9324 bytes)  
		MIME: application/vnd.in-toto+json
