## `amazoncorretto:21-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:53c899e52fca8bc147164385209a4038baa31dcea5b7f2c623befdd1218c59be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bd9934f758b7cdd448d38c101a786072fb45725aba8c255e32b5fc7e07f10911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228417227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ccad8a98d8e6c7dc68694d4df0f4ade2f00ed5b819288adb26d34a6157d672`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY dir:15f372c0d55f5152b222fa508a1a8c382d0621d72fdef0d2b746557a14bc0dd9 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:1e5e0347739e5468c65eed56d50fba90128674d8aae6fa196a8c01eeea145da9`  
		Last Modified: Thu, 18 Jul 2024 21:20:18 GMT  
		Size: 62.6 MB (62647926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad250b5732bbbc7bb1650e454ceee6651ef925a56bb1042f9615483b3d3e4775`  
		Last Modified: Thu, 18 Jul 2024 21:49:34 GMT  
		Size: 165.8 MB (165769301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:809321423f02f80dd824358195751ce7c33b513273c260a3e8e1a6b20ad0e8d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7494e88c35af38c68f41203d3913a82d7a00113268af388b998ade215a35c983`

```dockerfile
```

-	Layers:
	-	`sha256:d19fffa3dce3742dcb27305d27390fedd2c7cdd5a657a97d9aabc4d8e39b5df6`  
		Last Modified: Thu, 18 Jul 2024 21:49:30 GMT  
		Size: 5.5 MB (5527650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2e76dad4405b18883f4824e018fe873ea79f69ea233e6ac5a646a710a6db114`  
		Last Modified: Thu, 18 Jul 2024 21:49:30 GMT  
		Size: 11.0 KB (11009 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:621cc16ef07e654c25ca38246f377a511cf7d1042e7eb363b6b3c4ab83c8c7f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228401651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f428b4d515e8e61a74910e0be51ae90a1f9378efd255252520e57b7db9a2cd10`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY dir:cdeeb89e10fdbe3f38b9e5f6d359ee1afb9caaa1018fdd71fd6c0374dc592a5f in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:4ba2ef523fa6e28aa5a068ecb9167a3b9efa29481c3ecc6d34fab1c350b98b6d`  
		Last Modified: Thu, 18 Jul 2024 21:40:02 GMT  
		Size: 64.6 MB (64575311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1609bd2184809b739da413e633f5601c72bc3556d78906f97f51ea40ece2c5`  
		Last Modified: Thu, 18 Jul 2024 22:59:14 GMT  
		Size: 163.8 MB (163826340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:89ad1e22d5449f63c9524374dafc519c67c3e077eb5e57a985af1eaa59bb064c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5537696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3809e9f3b780ada370e9775240e8b536caf5afbfd67b3c2cb07b4a7d40ac0ed2`

```dockerfile
```

-	Layers:
	-	`sha256:86f0c0d87a6a40892f5e43f792ae7b7a61b091edf4d48937f726ea5d9275708c`  
		Last Modified: Thu, 18 Jul 2024 22:59:11 GMT  
		Size: 5.5 MB (5526337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6adc780e35803835131488059336963df3cea32081ebdd314eda1e6144be670`  
		Last Modified: Thu, 18 Jul 2024 22:59:10 GMT  
		Size: 11.4 KB (11359 bytes)  
		MIME: application/vnd.in-toto+json
