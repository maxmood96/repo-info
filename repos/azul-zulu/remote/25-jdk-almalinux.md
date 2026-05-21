## `azul-zulu:25-jdk-almalinux`

```console
$ docker pull azul-zulu@sha256:7a1f766f7c5fa79b5f384b831f9f3d6e3b51fd89d032bcc695cd90bc823aa7a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-jdk-almalinux` - linux; amd64

```console
$ docker pull azul-zulu@sha256:e0f05f8bc2e3d347a013d265804cf206ea9110a1352b7e1b416f8d66dba8216a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252985726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c46e05fc7fe91aa508e40ce1458c9244597af5ffdaa636d9ef96b545795932e5`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 May 2026 16:40:22 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:22 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:16:02 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:16:02 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:16:02 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu25-jdk-25.0.3-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:16:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Wed, 20 May 2026 21:16:02 GMT
ENV PATH=/usr/lib/jvm/zulu25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 21:16:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e0ca4bc012c6270dd0dab29783ab29d65b691d6b8f3ca1a92c5a8bfe9d51019a`  
		Last Modified: Mon, 11 May 2026 16:40:39 GMT  
		Size: 68.5 MB (68456602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3731db9b2705e5bab92b7866b2bef0d369b5292ab2a1b0ecedc3d132b3249d24`  
		Last Modified: Wed, 20 May 2026 21:16:20 GMT  
		Size: 184.5 MB (184529124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jdk-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:4fbbf7a4e08a143c3adfe2a64453d90e17be61ba7717ec34dafeabe8bc4311f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2798c475f06da5260c43564d2ed733193095ec2c42a23a692fe2943059f252`

```dockerfile
```

-	Layers:
	-	`sha256:ab028c1fd911ee3d5f43741905cf7f468bd176e3601f672b8c128eafb719ba0d`  
		Last Modified: Wed, 20 May 2026 21:16:15 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-jdk-almalinux` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:ba6dc30f65c4aa947297b09cb8949908ad28b52cc4d517a14d40e3984b71c7e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250649353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0273fe6a8aa1bd76c6aeee978d3ff2fb1597a6777f03a536b868ca2e7e98329`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 May 2026 16:40:15 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:15 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:28:29 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:28:29 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:28:29 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu25-jdk-25.0.3-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:28:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Wed, 20 May 2026 21:28:29 GMT
ENV PATH=/usr/lib/jvm/zulu25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 21:28:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:130dad5a52e276fdeb93dfac0bfa9126abc7121797fc1d218ebf01cf7201f1f0`  
		Last Modified: Mon, 11 May 2026 16:40:33 GMT  
		Size: 67.0 MB (66970169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e24788035c6d4d11f5aa2f0a275f9090252bd49131f0f129f71fe01e8d794d`  
		Last Modified: Wed, 20 May 2026 21:28:49 GMT  
		Size: 183.7 MB (183679184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jdk-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:70063d24f7208f0b699398b5af69ad932ba476d690d01ede9569a50ac1203db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a12de760677ed6a18cb28c4c2f564aa5f459b63401a1a29dcccc41bd70c8f67`

```dockerfile
```

-	Layers:
	-	`sha256:ab1c04c1730102913e253fc106982cd322425904af9fd258350d016769a6ebcd`  
		Last Modified: Wed, 20 May 2026 21:28:45 GMT  
		Size: 9.6 KB (9578 bytes)  
		MIME: application/vnd.in-toto+json
