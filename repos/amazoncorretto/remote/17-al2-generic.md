## `amazoncorretto:17-al2-generic`

```console
$ docker pull amazoncorretto@sha256:356dc09f6e299048b4bdc552e6dab1e0b27b005dfd1ce82a65fc74477469184c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c946d7745aa127ca2cabda543ac8e4475a0a6850fbfb8217dcbf1fb59ec174c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.6 MB (215623601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a81fa6f167a35967369c2562c9efdaf19d6ce014466ddc6756fcb03f4543b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:21 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:21 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:33:55 GMT
ARG version=17.0.19.10-1
# Wed, 22 Apr 2026 21:33:55 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 22 Apr 2026 21:33:55 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:5a3a1a219789b0285ea1d6a41ad03e6fab76f369592968c458dbfffd408719dd`  
		Last Modified: Thu, 09 Apr 2026 08:25:08 GMT  
		Size: 63.0 MB (62955266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88fb7f275c3da2b5b5b7b31eb708d54760cb55c59f84b71bc28f50840ed93d`  
		Last Modified: Wed, 22 Apr 2026 21:34:15 GMT  
		Size: 152.7 MB (152668335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6a20ebc6ec8e9112248430b6c52b66dd28804830cfa453a62fcaa93b3a04abdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5547830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eebde61289a57d51083b0643c5603c2eaa2910f9dbfd6c185ba15f4364a2733`

```dockerfile
```

-	Layers:
	-	`sha256:bb16a106018918af9668ecfffc4e07de13eac77cc122a7eb9ba0cdfeef5c95dc`  
		Last Modified: Wed, 22 Apr 2026 21:34:12 GMT  
		Size: 5.5 MB (5536617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:617f7d7da23c19c99462291244bf0655ec0b6cd7fea23dfd9e29f62549de13ca`  
		Last Modified: Wed, 22 Apr 2026 21:34:11 GMT  
		Size: 11.2 KB (11213 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5b0a439157e533257c7bb4060e7ce171639d67835bbc2d1d3fd3aff214da698b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.1 MB (216110321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4633ae68a6a306c13e83a12d4326facc2386d1ef518a835c726ee4a83cae44ab`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:35 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:35 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:33:50 GMT
ARG version=17.0.19.10-1
# Wed, 22 Apr 2026 21:33:50 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 22 Apr 2026 21:33:50 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f1f2697b3535de3cb27d338e724d6283baf064a258669349257ede7e5670fff3`  
		Last Modified: Thu, 09 Apr 2026 08:25:15 GMT  
		Size: 64.8 MB (64802975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db8f1938acd5a985de0803e9f8dbb51e0927c7676a3fa6b2f6dde4bd452a26c`  
		Last Modified: Wed, 22 Apr 2026 21:34:11 GMT  
		Size: 151.3 MB (151307346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1a145f1a5de8a121288fc8bd006ee470ea19cb4a9ddf341bdf4840ac23a27f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f537c7c00fb7b3fd4ef4a92e6c6d569f1505abc563f8497ee4ce6f76b3df129`

```dockerfile
```

-	Layers:
	-	`sha256:fe7ba9c41041f027b705aa63f39a791d778a33335944441add943f6e5e4b0c54`  
		Last Modified: Wed, 22 Apr 2026 21:34:08 GMT  
		Size: 5.5 MB (5535306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc393ddc57a641d6fec186ac285ae398301ff0c65d38a7903ef7a4206996c2b1`  
		Last Modified: Wed, 22 Apr 2026 21:34:08 GMT  
		Size: 11.4 KB (11365 bytes)  
		MIME: application/vnd.in-toto+json
