## `amazoncorretto:11-al2-full`

```console
$ docker pull amazoncorretto@sha256:4583615b8e8cd64b884da66ee9a57c56b8233ef257315854f7c56e431039f572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ee0e7c29bbd0922732732d9bb26021c2bb038b014e852ce34d9cd00bc3718295
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.7 MB (258708559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88020def6c819e1f60eea59938b3739e816d8f2fe8398cdcaca0f99a3b5fb662`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 21 Apr 2020 18:22:56 GMT
ADD file:c64a7d77d1e9f4364c8d2009059cb8668697d61f54f457215b6be6f0c9cded5b in / 
# Tue, 21 Apr 2020 18:22:56 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2020 18:51:29 GMT
ARG version=11.0.7.10-1
# Tue, 21 Apr 2020 18:51:52 GMT
# ARGS: version=11.0.7.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && yum install -y fontconfig     && yum clean all
# Tue, 21 Apr 2020 18:51:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:a3f8e652bdc470bbea38766fe41f8f12b9e4d44e9ce4037eb502839754b06b9c`  
		Last Modified: Tue, 21 Apr 2020 18:23:48 GMT  
		Size: 61.6 MB (61619066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8895c8298f706ca1c28f7501761d81a75f5c4c4f92866c8e4953fb2f85f745`  
		Last Modified: Tue, 21 Apr 2020 18:52:41 GMT  
		Size: 197.1 MB (197089493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9174b0a453c57a71401b937bfbfed4050d0d19b7e70dd0f96c33d2e30f06ebf3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.0 MB (258976951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0248db677943bb27ef9a8f40dcd8a0df2c4d0ca06cf1d3c27f19b7d560133a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 21 Apr 2020 18:58:16 GMT
ADD file:85fc0908f460f80c41755d2b5ab9ff6a025bb2726628ccc4edceb21d2e3f8edf in / 
# Tue, 21 Apr 2020 18:58:18 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2020 19:26:46 GMT
ARG version=11.0.7.10-1
# Tue, 21 Apr 2020 19:27:27 GMT
# ARGS: version=11.0.7.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && yum install -y fontconfig     && yum clean all
# Tue, 21 Apr 2020 19:27:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:0a37a5cd26f245ce54aff575389ef7765520d37d3ea7c437144c936c6adffc8a`  
		Last Modified: Tue, 21 Apr 2020 18:59:54 GMT  
		Size: 63.1 MB (63079760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64c950fe960e43578caf850fca203e641f2b3deeb231129de3a6803c1538561`  
		Last Modified: Tue, 21 Apr 2020 19:28:58 GMT  
		Size: 195.9 MB (195897191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
