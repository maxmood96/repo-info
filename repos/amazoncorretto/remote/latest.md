## `amazoncorretto:latest`

```console
$ docker pull amazoncorretto@sha256:1f311acf91a95cd0b416497f54b44c739913032b7a83f612e8373dc3cc52048c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:latest` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:cc2ad2c0538a87c081a23ac2fb8a026c6afc7db967aaec5c85e767a92b14701a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138255406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487f104631fddbf84c286477bae13e1033d9549c6e8db8ee2f127d8645891a48`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 02 Oct 2024 22:07:55 GMT
COPY /rootfs/ / # buildkit
# Wed, 02 Oct 2024 22:07:55 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=1.8.0_432.b06-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:f956a2176a592b2f85941102c85f1a745c5e74f263c66fc5212bf9eb619f28e1`  
		Last Modified: Thu, 03 Oct 2024 13:25:55 GMT  
		Size: 62.7 MB (62678156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05cb8961ea76f5971b7a6a880683b7a13150fa967d716f14802e9f5e52939634`  
		Last Modified: Wed, 16 Oct 2024 17:56:10 GMT  
		Size: 75.6 MB (75577250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:latest` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c89a3d5a19178025a906a29263f65519a616fa50e71b71fec9bed00ba5ae1034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5381344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d2cd0e10892fcab56ea96475d550830f24ca947c65b8721697742d6125344f`

```dockerfile
```

-	Layers:
	-	`sha256:f45d092f0079aaebf101e2a8f86552e6e6887659fa396d0df23af0e12f4232ef`  
		Last Modified: Wed, 16 Oct 2024 17:56:09 GMT  
		Size: 5.4 MB (5369771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3507764b2235ca73263214122cd5f371deb846cb98ad8436163237471a08049`  
		Last Modified: Wed, 16 Oct 2024 17:56:08 GMT  
		Size: 11.6 KB (11573 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:latest` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:cb97e90de12d4403b7c1180d020aa6de775f3ca4cb95f849f12a6b28c4faf483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124266253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854540e55be5e2eabf2c8286e1deecdeee13503ed4353936041e38496ae1bc1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 02 Oct 2024 22:07:59 GMT
COPY /rootfs/ / # buildkit
# Wed, 02 Oct 2024 22:07:59 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=1.8.0_432.b06-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:17d30073c92a41fbc086cf7be6bbf70600b21ad41c671459f9fd5c536e5182dc`  
		Last Modified: Thu, 03 Oct 2024 13:26:09 GMT  
		Size: 64.6 MB (64592659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9b548757d8bb6db947dd4d657181463e97bd84099f1ad932baa8c536d42269`  
		Last Modified: Wed, 16 Oct 2024 17:55:47 GMT  
		Size: 59.7 MB (59673594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:latest` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:aead205594b67bae9c19dff8042dfe9f8fdb4cbc98891cd71b29b38cfc0c1bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f511815df24a954a6c6773544c5e968bb08115addea025116eecc467256e5c86`

```dockerfile
```

-	Layers:
	-	`sha256:ce79d1e3a67777da844e5e172163f558ea377bb800d3a733753b14db23ea1378`  
		Last Modified: Wed, 16 Oct 2024 17:55:46 GMT  
		Size: 5.3 MB (5348298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad2da357d0948220adfc64cccc59bb949ceba0352e647012b4cbe9dd29969c97`  
		Last Modified: Wed, 16 Oct 2024 17:55:45 GMT  
		Size: 11.7 KB (11738 bytes)  
		MIME: application/vnd.in-toto+json
