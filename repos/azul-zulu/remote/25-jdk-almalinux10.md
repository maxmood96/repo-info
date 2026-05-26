## `azul-zulu:25-jdk-almalinux10`

```console
$ docker pull azul-zulu@sha256:deed912d93d7fe7334711cfcedc84020073725a6c8d27ac458abf0a27d69bfa6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-jdk-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:ef8eccb629c8ade213a06e9f89f5c652f19d743373282ef1889b2b1a33a76e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252982333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a463808498f47a8a6179eab43a855b83d433c77143b9ce4be518d8393be951`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 26 May 2026 19:12:04 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 26 May 2026 19:12:04 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:18:34 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 26 May 2026 19:18:34 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:18:34 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu25-jdk-25.0.3-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 26 May 2026 19:18:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Tue, 26 May 2026 19:18:34 GMT
ENV PATH=/usr/lib/jvm/zulu25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:18:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e00696cab286036acbc1819dc14bffffe3d9b62859baec766357c34271aa510c`  
		Last Modified: Tue, 26 May 2026 19:12:20 GMT  
		Size: 68.5 MB (68456037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6960e511e9a2c9c4837d554d463f5c811fb6f29e3e0c80a89cffecfed365a07b`  
		Last Modified: Tue, 26 May 2026 19:18:53 GMT  
		Size: 184.5 MB (184526296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jdk-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:c3a3be14da3c09f9abd64196b730786b10bd3d86a446635ac13a619267a76428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cde0967d88f5cf08600861e2bb14d3bf94d6cff2ef1ce169174b3070b94d028`

```dockerfile
```

-	Layers:
	-	`sha256:7496caf4400e25de808c02875e4a61d3c67049042578f33928412f02467b5bec`  
		Last Modified: Tue, 26 May 2026 19:18:48 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-jdk-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:530a88fa3fed9e5bfbc1131a30ba5b9045d36744ec4fb7723dcda04f5aed524c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.7 MB (250650847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ce7290f23f1fc66706dd502395dca38078326c4e15ed1c8b76af9d54b12afa`
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
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu25-jdk-25.0.3-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
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
	-	`sha256:348d420f2dd1a6363fc1162571bd3c41ad0a302ae28f473f79d0fbc55341259f`  
		Last Modified: Tue, 26 May 2026 19:19:01 GMT  
		Size: 183.7 MB (183679955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jdk-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:d1203b8b0df576b5b6f790f154ec0788fd6555c16fadaf70f7eeceefb0f3feea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e0a8dc0fc5e001b0927e5acc94d1427b57cd665229ffb2c2fcda787cc12a2c`

```dockerfile
```

-	Layers:
	-	`sha256:ecae52344da183a52d467b58200170d391f5659dfb28e0d13e887f0de851dcdc`  
		Last Modified: Tue, 26 May 2026 19:18:58 GMT  
		Size: 9.6 KB (9579 bytes)  
		MIME: application/vnd.in-toto+json
