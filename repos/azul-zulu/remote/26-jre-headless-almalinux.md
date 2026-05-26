## `azul-zulu:26-jre-headless-almalinux`

```console
$ docker pull azul-zulu@sha256:ebf3195d87426c373730208b973091ab72a05e301f3398fa0229dce99570142e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-jre-headless-almalinux` - linux; amd64

```console
$ docker pull azul-zulu@sha256:f31baa718c11fc0c3726ebd37b6b4c63339bb50a4a03a82fa974708069657967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.5 MB (159523909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39c1f2e0d29fc7dacdf8a77be4faea6a1147217c538b6a7321924642f6626e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 May 2026 19:12:04 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 26 May 2026 19:12:04 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:18:51 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 26 May 2026 19:18:51 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:18:51 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu26-jre-headless-26.0.1-1;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 26 May 2026 19:18:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Tue, 26 May 2026 19:18:51 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:e00696cab286036acbc1819dc14bffffe3d9b62859baec766357c34271aa510c`  
		Last Modified: Tue, 26 May 2026 19:12:20 GMT  
		Size: 68.5 MB (68456037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22c3906d6b8beb0050dc164023e910e6451072dac584f8476c4bb6f4ce710a7`  
		Last Modified: Tue, 26 May 2026 19:19:04 GMT  
		Size: 91.1 MB (91067872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-headless-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:3a0a6edcce5a63ce9c1d5e870c6645908b111481dc1c298c70b9e2b508888207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07a166b3880b4188903555b7fa9af9e9029683d34dfdd6fc680867c8cc2e92c1`

```dockerfile
```

-	Layers:
	-	`sha256:3c03fe45df7087c1b998abc1a3b2e94506f676f43c6b42ce849b5eddd7259f49`  
		Last Modified: Tue, 26 May 2026 19:19:02 GMT  
		Size: 9.2 KB (9230 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-jre-headless-almalinux` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:802c9e38203e20a2cc2d7da12aefe63b27c3a2136851da07018b5199edd0a256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 MB (157967856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa27a45b93d71ac2f858b026a96b61d2692da9b54014dbd4230dde8cbf460626`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 May 2026 19:15:08 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 26 May 2026 19:15:08 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:19:04 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 26 May 2026 19:19:04 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:19:04 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu26-jre-headless-26.0.1-1;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 26 May 2026 19:19:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Tue, 26 May 2026 19:19:04 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:b1228b076bddc8d6b69c35f53b57866988d02e0877190f42b0390db4a24d6bba`  
		Last Modified: Tue, 26 May 2026 19:15:24 GMT  
		Size: 67.0 MB (66970892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7185ec0918b499b4e22d34676aa3414c53015549e445ccb54f6ec288ed62d80`  
		Last Modified: Tue, 26 May 2026 19:19:20 GMT  
		Size: 91.0 MB (90996964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-headless-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:b2bd54e1cc576ada407757622227f1a6ff77b74ee80ff4e4bce1cde5b9f593fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c53d746f5553f3c93fb49d0c22c43f2429d800b82f5f52fd64a5d76c25b5cf`

```dockerfile
```

-	Layers:
	-	`sha256:4ba676353435a4b3c47174fbc4c681e7b4dce2c77023e1e217524e3fffe005bd`  
		Last Modified: Tue, 26 May 2026 19:19:17 GMT  
		Size: 9.3 KB (9323 bytes)  
		MIME: application/vnd.in-toto+json
