## `azul-zulu:26-headless-almalinux`

```console
$ docker pull azul-zulu@sha256:30c2d806b471bd394015f43e8b2659f8fa5c41ef32f8b590d5c67c64c2d6291b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-headless-almalinux` - linux; amd64

```console
$ docker pull azul-zulu@sha256:87ccabeba11b18e0e0087d785ba566b65f11499de30278c7298f3671dc6c2128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254657640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:393dedf626d7b5affa8e232f95591dea751bce7f40d975053307ac2594689c96`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 May 2026 16:40:22 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:22 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:16:08 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:16:08 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:16:08 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu26-jdk-headless-26.0.1-1;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:16:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Wed, 20 May 2026 21:16:08 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 21:16:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e0ca4bc012c6270dd0dab29783ab29d65b691d6b8f3ca1a92c5a8bfe9d51019a`  
		Last Modified: Mon, 11 May 2026 16:40:39 GMT  
		Size: 68.5 MB (68456602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0948fab3f3ab2b34a0d496cedbf811aab8d15f4eb1effbc6a3b8ac10ae4472b5`  
		Last Modified: Wed, 20 May 2026 21:16:26 GMT  
		Size: 186.2 MB (186201038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-headless-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:5a781c692f4311b7ef566d81530bc85360b2a7625f70eb557954d898e156ada7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64c5e314591821410843086a35e8fc6cd7c7e475b6fe7b917117b2447f9f268`

```dockerfile
```

-	Layers:
	-	`sha256:16579b68f759279da418fa5fa16e5525b1d0daf1e0c222f5c164d52413cefcf8`  
		Last Modified: Wed, 20 May 2026 21:16:22 GMT  
		Size: 9.2 KB (9232 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-headless-almalinux` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:453e148fc807fbdeacbe601d220e192bb4b2700561fca2ed0bf46d5f2d6a1ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.9 MB (252871113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd1ea76a553cb6252f3646da06cc4893e611341629535ad0bf9c5f09df3c77cb`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 May 2026 16:40:15 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:15 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:29:01 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:29:01 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:29:01 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu26-jdk-headless-26.0.1-1;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:29:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Wed, 20 May 2026 21:29:01 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 21:29:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:130dad5a52e276fdeb93dfac0bfa9126abc7121797fc1d218ebf01cf7201f1f0`  
		Last Modified: Mon, 11 May 2026 16:40:33 GMT  
		Size: 67.0 MB (66970169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e0e5d26517f2136f6adb059ff1be74884315c1aebd832287ed11896cd14b2e`  
		Last Modified: Wed, 20 May 2026 21:29:21 GMT  
		Size: 185.9 MB (185900944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-headless-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:6804947cf9f5435f19d5d253c3ea72deb98ecff2caf931cab2385172a46b4c9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2978d907218339ddd7dc9ab81115b9d59373e253d24811d2587311bf3c1e67b`

```dockerfile
```

-	Layers:
	-	`sha256:d1f85cfabb2db903600288a70e2f45bb17b7eddd20faec998ba814acdd638c36`  
		Last Modified: Wed, 20 May 2026 21:29:17 GMT  
		Size: 9.3 KB (9324 bytes)  
		MIME: application/vnd.in-toto+json
