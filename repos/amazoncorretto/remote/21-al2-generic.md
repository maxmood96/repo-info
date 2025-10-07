## `amazoncorretto:21-al2-generic`

```console
$ docker pull amazoncorretto@sha256:4599af808338fc153b3d921e5e85797a477320cb677d5c672390b790159eebd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bdcb08452710c286e6090de034de8bddafe2fdef6da27ca974424f2e08ba1eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (227991599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eb778d158131e70723d545dc9ea4e7e9e2b04bf7ee4a16e358feb4c727e6d7c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=21.0.8.9-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=21.0.8.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:91f0f90aeef889cedc2e056e6976319ec5d96df70bf35b1d46092d2c1f375f2b`  
		Last Modified: Sat, 04 Oct 2025 04:29:16 GMT  
		Size: 62.9 MB (62940620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abd3da4721c571a064607ac8230042118beba854149f9b89f55bb43cb1512a6`  
		Last Modified: Mon, 06 Oct 2025 22:11:19 GMT  
		Size: 165.1 MB (165050979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d301f76bb1a601cd8b057688a030a58b9291d2a3c985ace9f29d8d034cb77f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5543612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9685de18bf1f674cbefc1b3f6f0f9462be1fadde86505cd7ff5c1269483c505`

```dockerfile
```

-	Layers:
	-	`sha256:3df16a256c62426870c25643cdf8f42215587e95c9ace716e8702ba2ddd89f49`  
		Last Modified: Mon, 06 Oct 2025 23:15:49 GMT  
		Size: 5.5 MB (5532364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e90faf3f1dd483d17f57b12dba8002ceb2646501d2d88fd3f2e1814330642f40`  
		Last Modified: Mon, 06 Oct 2025 23:15:50 GMT  
		Size: 11.2 KB (11248 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5bed7db9a213212ec68232d6de2958513364cd972ab126e23cc59a563525d77a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227905832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd697640eef4e1acdb3e8ef2ae2050e00fc703aec241003a2d2f338aae7eb887`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=21.0.8.9-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=21.0.8.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:8b6c0dce7361457a1cee4518c5dc9c75ff3fa343c4460bdb254d7bd18bc1bf03`  
		Last Modified: Sat, 04 Oct 2025 18:25:08 GMT  
		Size: 64.8 MB (64793208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3602182be132a4d99034a4d5d48cb562b07140ee58186cb12024f7f5df2c29d`  
		Last Modified: Mon, 06 Oct 2025 22:12:36 GMT  
		Size: 163.1 MB (163112624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5f8c317f18f9ac42abd23a3e9a926adba048a6dd61ae449138583b68a92c3c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5542453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e47434b92d94c1e3df45c564dd2d10605684f82294392273ecb99b92d2b3e58`

```dockerfile
```

-	Layers:
	-	`sha256:5040f479d2cdf6e9c85fc07ddc66b081e561dae64df32f7147a069e4713849c1`  
		Last Modified: Mon, 06 Oct 2025 23:15:54 GMT  
		Size: 5.5 MB (5531053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cb5b9df2ad4c9556c9f7471905b296e08f16a63f9bbaef1eda897c1f208a085`  
		Last Modified: Mon, 06 Oct 2025 23:15:55 GMT  
		Size: 11.4 KB (11400 bytes)  
		MIME: application/vnd.in-toto+json
