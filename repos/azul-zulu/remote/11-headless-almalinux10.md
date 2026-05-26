## `azul-zulu:11-headless-almalinux10`

```console
$ docker pull azul-zulu@sha256:309b60afdf0a3803da3229d3c1b2b6ecbf0b633edc017d2051ca8519ec489727
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-headless-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:a10e9f24b18744bb8959f4d076e5e0b993794b448ce2368c8555d80a2d957222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.6 MB (215629402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f75616231cd99511dbcce697ce63b805399d86487b1816c026f6dc3dc0c641`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 26 May 2026 19:12:04 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 26 May 2026 19:12:04 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:17:51 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 26 May 2026 19:17:51 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:17:51 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu11-jdk-headless-11.0.31-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 26 May 2026 19:17:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Tue, 26 May 2026 19:17:51 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:17:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e00696cab286036acbc1819dc14bffffe3d9b62859baec766357c34271aa510c`  
		Last Modified: Tue, 26 May 2026 19:12:20 GMT  
		Size: 68.5 MB (68456037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d294567f8edbe5aa5ec4147f31bb4efb78931b5a3b3b0b33f512ce03d9a0fd61`  
		Last Modified: Tue, 26 May 2026 19:18:06 GMT  
		Size: 147.2 MB (147173365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:e20357b59e0f6b862969b9ef51476f1d869f3871667449e84a62ba22b890f388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546c73b63fe1e0f19a3210d117b32098fee03772dd5d86a92b062af0fd7be308`

```dockerfile
```

-	Layers:
	-	`sha256:5d980f99aa3e6b9bf2ce49357789d75f50b632bbdcbc4834dfb3ed7cc8fd1f51`  
		Last Modified: Tue, 26 May 2026 19:18:02 GMT  
		Size: 9.2 KB (9238 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-headless-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:376895949102d675bde10092e9e44aa4798bcc11f240ca37c451925cdb96d3da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213827457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778b6d1fb272b986f9ac72f88902de3d7221d2e9e0b814d8f2c0ee9b0ddacd40`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 26 May 2026 19:15:08 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 26 May 2026 19:15:08 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:17:59 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 26 May 2026 19:17:59 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:17:59 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu11-jdk-headless-11.0.31-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 26 May 2026 19:17:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Tue, 26 May 2026 19:17:59 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:17:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b1228b076bddc8d6b69c35f53b57866988d02e0877190f42b0390db4a24d6bba`  
		Last Modified: Tue, 26 May 2026 19:15:24 GMT  
		Size: 67.0 MB (66970892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dbe0c20f50b1a016772f4a55ba75d92c4fd8da8f66480c9a9cdee44a432097`  
		Last Modified: Tue, 26 May 2026 19:18:14 GMT  
		Size: 146.9 MB (146856565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:6d92c347da55b3725bcfa7f5a5255a7ba1240e8bbdbe75ee541c10f115dbe283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0432b389a8fc215dc92ee648e983429fc4a9d3010f994c23ccb8f7ec0818cc29`

```dockerfile
```

-	Layers:
	-	`sha256:63e1bdd0ad46a4713f33306515a9df9807137400c6f1354399a477f75c5420ea`  
		Last Modified: Tue, 26 May 2026 19:18:11 GMT  
		Size: 9.3 KB (9331 bytes)  
		MIME: application/vnd.in-toto+json
