## `amazoncorretto:17-al2-generic`

```console
$ docker pull amazoncorretto@sha256:1c4922080f55a03925b39012e8c34c0bea4e25e3e3df2276f5e0080a50d80b5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e9d41c195b70fade0223623ea31f3d110ea34158462dee3f1d3c85deb6580b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.6 MB (215620800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70298ea1c8b73e7be6af70214c0154b769237992acc7708492e66270f9f6de7d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:59 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:59 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:14:18 GMT
ARG version=17.0.19.10-1
# Mon, 22 Jun 2026 18:14:18 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 22 Jun 2026 18:14:18 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:14:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:b5a31d0a32c9342b5b53f098c4d8ac4fadeb6cbc6b34b2e4424fd39eb880bf9a`  
		Last Modified: Sat, 13 Jun 2026 04:09:34 GMT  
		Size: 62.9 MB (62942019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91bfd2599ba044359e57f7483de74c4605efe350141bbeb5e51bfa4a3c23b9b`  
		Last Modified: Mon, 22 Jun 2026 18:14:39 GMT  
		Size: 152.7 MB (152678781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:258ee3a06bd53dca3d49d51b21ff58efee428fdbf9a2aa66533c81f0b9522e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5547830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb5dfac217e5af7a618575e53a6236c865bc1701b15cca015bcc8458061a314`

```dockerfile
```

-	Layers:
	-	`sha256:d3fc52d510ea46552742b393b8d64ec28f8a5edc61f1f55dbaa7bce53fce72b6`  
		Last Modified: Mon, 22 Jun 2026 18:14:36 GMT  
		Size: 5.5 MB (5536617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4123f8a08da4d7faa77c5c58d5cf8c2b4535d79b1c7ef4c1b971f52e0ffcf80`  
		Last Modified: Mon, 22 Jun 2026 18:14:35 GMT  
		Size: 11.2 KB (11213 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5d48482ef3d3dad563681241474282d218e946c80a8721a5e5f839db87467a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.1 MB (216072112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06fc8b3e2ecef43bb175625e233bf0bcf5566c58bc1d3fc20243d19561b56133`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 18:00:28 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 18:00:28 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:14:16 GMT
ARG version=17.0.19.10-1
# Mon, 22 Jun 2026 18:14:16 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 22 Jun 2026 18:14:16 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:14:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:4b30ecc040ec91b7e580ef7f93f591eaf80422b110a473c44b4d0dbcb2301395`  
		Last Modified: Wed, 17 Jun 2026 13:06:48 GMT  
		Size: 64.8 MB (64794736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0d804c084121f03b54fc16c0bdbdcfd660261c53137d6c83b654614d5f7772`  
		Last Modified: Mon, 22 Jun 2026 18:14:37 GMT  
		Size: 151.3 MB (151277376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a0fb365991272cd4b360a5db0e65b508b76f11f03bab5cc7788b39d5e76fecd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb36a02c5b3ae18700fb1c65acdacd64dbef131d3d21f0c8e384a850e159fcd`

```dockerfile
```

-	Layers:
	-	`sha256:dba3e828facd97d155a2013e15c438755185ce42f57acbece40f15b6ed7ae689`  
		Last Modified: Mon, 22 Jun 2026 18:14:33 GMT  
		Size: 5.5 MB (5535306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:444bed52f1d8b5d2954a562665a5496ce155df9bd80c4ffc90f276b6f6adb8c2`  
		Last Modified: Mon, 22 Jun 2026 18:14:33 GMT  
		Size: 11.4 KB (11365 bytes)  
		MIME: application/vnd.in-toto+json
