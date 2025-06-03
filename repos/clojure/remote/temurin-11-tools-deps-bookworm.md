## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:b647c3c61bf58f922ec326c6f94e212542c27ff24518521cff8524d4f0994465
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5da5380e4b413894a750182be7b071fe3e70f18448394f65adcb7d4958261b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 MB (275119578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0bdc12eb6a59c09209fcc8618e877375afd7d1b1d4715aff3d1b3ac4b5bee9`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d422aaca88411f296f86121286899d79d1fcbc7e3c0a5a8f16372016a229ce8`  
		Last Modified: Wed, 21 May 2025 23:32:32 GMT  
		Size: 145.6 MB (145635749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9209eebde0cf4e3049930da8b63dbda29d96976af1973be58126ae5f4203a6b`  
		Last Modified: Wed, 21 May 2025 23:32:35 GMT  
		Size: 81.0 MB (80994940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6863f987cb88a69681cf847b6393d8c781f1a5673b889aabf56e021cdbed16`  
		Last Modified: Wed, 21 May 2025 23:32:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d25666b2a20f0b2f93d58a548b5241830cc90b09ba0597ea76fae3b0d7cb07fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7252915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc48ef06459eb2d5c9d5ecd47789bf63ca0e5938b305317fce50fd9464253eb`

```dockerfile
```

-	Layers:
	-	`sha256:f5afefab26efdf25f37d449dcfff4b2657ecd293cb86fa88626101ea1803b7e6`  
		Last Modified: Wed, 21 May 2025 23:32:33 GMT  
		Size: 7.2 MB (7238663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:752c658e7b3bbb99c270952ce9aeeb4a35ff559956c2b89c03c6d962e92e5dc2`  
		Last Modified: Wed, 21 May 2025 23:32:33 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:229b51ad4d408285dab83e4f29cf2746f1eb4f90be185f97a096c3a0f6d91698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.6 MB (271595211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adbaf50ca33ef02fd14b548b4ba6efef78f8cd63d6fc5c4ac0d08c209dc0175a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682800a477954fe07fd9e841558f511dffb10fc0892f35d76669df1d97081e87`  
		Last Modified: Thu, 22 May 2025 08:09:34 GMT  
		Size: 142.4 MB (142420720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a014d244cc693a83ac405a6d68fbc8e67d1249a0b41af04a62ebe3299ef251`  
		Last Modified: Thu, 22 May 2025 08:14:38 GMT  
		Size: 80.8 MB (80846666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b2bd3fdec57256481b3482f92480dfe32b075c2137078d20baa065a0846a68`  
		Last Modified: Thu, 22 May 2025 08:14:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:90c327b34bf60ad2cfb5983ce879e31f0bc08451c07eae08161a332f96e0a7bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7259414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b845fef0302fe242db6de12b419ba99aebcf70e51714b374d7b087546889304`

```dockerfile
```

-	Layers:
	-	`sha256:69f936ba4cbb6100e62dd5e25828ad68416de89b54b47f720d86f13cc8aa41d9`  
		Last Modified: Thu, 22 May 2025 08:14:35 GMT  
		Size: 7.2 MB (7245044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c09a6860148eb828829542aa9198fcbe5964840b321015e4c234ac27a5bd374`  
		Last Modified: Thu, 22 May 2025 08:14:35 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:cfd4bebb7c13b495fdf6a21c209ff1d26d6fa3b70a160376674b33c95d48ba1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (271952446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72f3dd9ac5b327938158bde9c8b6f37748044fd0c817078e6f92417059d4aa05`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f36a97adbb773a3c08e782c79c4aca670897f01d3074352c92dbab72f06b22`  
		Last Modified: Thu, 22 May 2025 10:58:08 GMT  
		Size: 132.8 MB (132809819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e9c29fcc7dd55b9a5e82020524cf52d9b0e97e1bd48e2bad6dd22884842965`  
		Last Modified: Thu, 22 May 2025 11:07:05 GMT  
		Size: 86.8 MB (86810364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7402825a5b281f3f24ee010fc37666a61c976c341353e69cf4c73b9b334af9c`  
		Last Modified: Thu, 22 May 2025 11:07:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2abe720ec85bf634378e3cc9ac08d4b15bf9b2b7bbddd26079ab96ed7ee10a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7257552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0751aa4da0cefd7b88837a732914661d3b3066be0a81521a93004ae2b463cd9d`

```dockerfile
```

-	Layers:
	-	`sha256:1194480dd29fad31b42dc2c62fef9e1c267ae38f6d6db5dd84bc02dec33ac645`  
		Last Modified: Thu, 22 May 2025 11:07:03 GMT  
		Size: 7.2 MB (7243252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78b4757c916453a8c0745c5bf31ba07c533917c8affe6b1f0a9f830a61bf2a29`  
		Last Modified: Thu, 22 May 2025 11:07:02 GMT  
		Size: 14.3 KB (14300 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:4eac9df9c9e0d196e66d861cf80955c5b5382629573e7feefd224effb4bc4ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252519730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ce2a57f95eb9e3d696c03079ff637b7c194e11e400da9907a5fcfdc7ccfe67`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Wed, 21 May 2025 22:28:14 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86c88c5d926257cdcfb8a6708039fa40a0a893499f3bc0262b7011bfd58b087`  
		Last Modified: Tue, 03 Jun 2025 06:00:21 GMT  
		Size: 125.6 MB (125585354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524d530659b7bb106639d8da33cac4d09544c96b6487d31342adece1135559fd`  
		Last Modified: Tue, 03 Jun 2025 06:06:20 GMT  
		Size: 79.8 MB (79789891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300745607ad8c0bd8b44e478cd0f702a159f7d52170521e4624f9ea10ae5b4ff`  
		Last Modified: Tue, 03 Jun 2025 06:06:18 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:add5c4c21b851f996746d66f23ff79d006b003fa6f5fe2dc08d91530abbb4ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7247130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446b3c854b308a9e0f805b2444aee7101a3db1af294152fa6513ba6ffbf7cc79`

```dockerfile
```

-	Layers:
	-	`sha256:6142696d3926a54e37dc990fc3485e0d384763758e3d0084d2f15d87b83063f0`  
		Last Modified: Tue, 03 Jun 2025 06:06:18 GMT  
		Size: 7.2 MB (7232878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42327518181b085b667584dfbdae006bf5126d0fb6640e472d22d51f8989b79e`  
		Last Modified: Tue, 03 Jun 2025 06:06:18 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json
