## `amazoncorretto:21-al2-generic`

```console
$ docker pull amazoncorretto@sha256:0560910f891ef2d1277539b022de1f6c032d273f0f1e8444f45b7ef8005463c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:870e1648576bea4272e29cc79f8a4857c604af7557a5b0d658ce643def26d132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228508718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796e818f4822d6bfbc7fce9abcc2a2b6c4e9d8266ebaa1d6b24a1d3a3b8807cc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:26 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:26 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:15:29 GMT
ARG version=21.0.10.7-1
# Mon, 02 Mar 2026 23:15:29 GMT
# ARGS: version=21.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 02 Mar 2026 23:15:29 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:15:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:369d025c034936d3f19b9a4b859b983f355f304e2e95b16c4cbeb64c69d301c0`  
		Last Modified: Thu, 19 Feb 2026 18:52:05 GMT  
		Size: 63.0 MB (62960229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66bda24a0a1972d7430848f2e9c53e25d2db55ca3537798a384329ba70f9db98`  
		Last Modified: Mon, 02 Mar 2026 23:15:50 GMT  
		Size: 165.5 MB (165548489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9de946ddc2ab9fe49f70e0a402dcda8c2318f0f3504583d014b39679cf58e705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d37949e9a095e425d8429f2b52b7984ad0f9acad4b65a392225a56da15547c2`

```dockerfile
```

-	Layers:
	-	`sha256:158653f1f23f2e2bf9911a1108aa257435935e14df4e869d13373836e4f548c0`  
		Last Modified: Mon, 02 Mar 2026 23:15:47 GMT  
		Size: 5.5 MB (5535607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ecefe5471ba6657db81873d2e54f54c2eb8dfc69b6a2ccd557e1c55597d6897`  
		Last Modified: Mon, 02 Mar 2026 23:15:47 GMT  
		Size: 11.2 KB (11212 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b06a6e8e337d28989bb8745d00bb1341c275e14bba91a3fc738930c62fafdf75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228417536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0630a99582b6e5a6b5e3e2a7430b12b333b48fd838f89b9c37dd3aeb5798bb30`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:30 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:30 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:14:44 GMT
ARG version=21.0.10.7-1
# Mon, 02 Mar 2026 23:14:44 GMT
# ARGS: version=21.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 02 Mar 2026 23:14:44 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:14:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:ce260c9faa157afc8e59fa056130319824fd1c549b337649ecc964c38a8d7b19`  
		Last Modified: Fri, 20 Feb 2026 15:17:29 GMT  
		Size: 64.8 MB (64811411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cafa780b6d9640895d00c1754835e9116ebd6059e626cc1a1618dde104a8dedd`  
		Last Modified: Mon, 02 Mar 2026 23:15:05 GMT  
		Size: 163.6 MB (163606125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6f30ee6f05ee51bda2b093bf9c309b4d5c89b97fd44225cdea0a0e462f9953f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5545660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77cdecc9ab702ddf16b07a734395b3e4563a620e7dda9470cd202087b9abdff4`

```dockerfile
```

-	Layers:
	-	`sha256:bb03718d326e749b9c4a4c092646f28ba19fdcf4c85f0b70cf4831188f436c20`  
		Last Modified: Mon, 02 Mar 2026 23:15:02 GMT  
		Size: 5.5 MB (5534296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:063b8c6d38f29dac67ae00f110bdf15aa66ab2f7e00ffe02fe12585e0fc5f00e`  
		Last Modified: Mon, 02 Mar 2026 23:15:01 GMT  
		Size: 11.4 KB (11364 bytes)  
		MIME: application/vnd.in-toto+json
