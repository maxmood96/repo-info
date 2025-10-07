## `amazoncorretto:11-al2-generic`

```console
$ docker pull amazoncorretto@sha256:df429501e4738bb4ed379684e737e2291cf816d379e4b53eaeaaac35f67c9b0d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5feddab7313ae073c231c0d8fca2d991d3dfa54c08ead238cabe38a50e7ff9fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211237798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105bf6be05a7beba98a84d137cf276c77975acbbc0931818e17e6b5add41631a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=11.0.28.6-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:91f0f90aeef889cedc2e056e6976319ec5d96df70bf35b1d46092d2c1f375f2b`  
		Last Modified: Sat, 04 Oct 2025 04:29:16 GMT  
		Size: 62.9 MB (62940620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152c9b18b72b93cc14d31fcd5ae947987b35e6e81f265f08584038b95dc7093a`  
		Last Modified: Mon, 06 Oct 2025 22:12:29 GMT  
		Size: 148.3 MB (148297178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fac68aca609d0ab80064f0c7bb1ea007a2911718bf3d72c5b9b47682c13392ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5551033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6071c23acd785d3e0db0b5f85fba428a22af70e539a0a746e29f42de115aad8`

```dockerfile
```

-	Layers:
	-	`sha256:9ad12156561362a221f5be4a6863fd2b939302e9aad398e049f734e1eee1b6f8`  
		Last Modified: Mon, 06 Oct 2025 23:15:58 GMT  
		Size: 5.5 MB (5539778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:111a47eacfd0afb32f925dd40bf7e366bcb261062d03e36af92347fe0f1f9a4f`  
		Last Modified: Mon, 06 Oct 2025 23:15:59 GMT  
		Size: 11.3 KB (11255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8647ed1a9a9b726a7effb340e74073d6785765d62654f53e581e507eaf90bc05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210165811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0730beeff2285ef2db66efc8861fb11eea6393749aee18a6ce7d387d38a344dc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=11.0.28.6-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:8b6c0dce7361457a1cee4518c5dc9c75ff3fa343c4460bdb254d7bd18bc1bf03`  
		Last Modified: Sat, 04 Oct 2025 18:25:08 GMT  
		Size: 64.8 MB (64793208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18f29a76c4aa2e6026e14aef8f8ac084f68d3ca8907802097cb0996a18302af`  
		Last Modified: Mon, 06 Oct 2025 22:10:55 GMT  
		Size: 145.4 MB (145372603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:34936bd68c7c612ee7accb52a1116e96f328fed9328fc52780285b84283b4206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5550679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c41f0c343389dae833de7745a18eb2ed532bed20fb08756b554b555752599d27`

```dockerfile
```

-	Layers:
	-	`sha256:c84be54bd07a5d0d3bf4492abd19dff8776bd27bdd241e54095d2db281bb6585`  
		Last Modified: Mon, 06 Oct 2025 23:16:00 GMT  
		Size: 5.5 MB (5539272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8298d31ce231a9a18a97abbd4f51a9dae99962543d003ce22eff7ac9120d21fc`  
		Last Modified: Mon, 06 Oct 2025 23:16:01 GMT  
		Size: 11.4 KB (11407 bytes)  
		MIME: application/vnd.in-toto+json
