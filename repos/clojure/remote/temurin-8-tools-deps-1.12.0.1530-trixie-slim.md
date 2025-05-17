## `clojure:temurin-8-tools-deps-1.12.0.1530-trixie-slim`

```console
$ docker pull clojure@sha256:613eb1e13d27722c3ec034dab3c8a549bb9b8f09a9b84a5327b9e0cf5d17c5ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1530-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:52b3fccba2d6ee329de130eb0b9c68de9800e00de1e73cf3eccb32f3e71b447e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156194574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb5691894aee49640831d2d69ffecd74e0863a58d2c507e37e999aeb5391b7b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1745798400'
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
	-	`sha256:3ae34fc80ed56f2b3a9a0b682b58e28e57fe981f5e514c3f687044f4b967608f`  
		Last Modified: Thu, 08 May 2025 17:06:40 GMT  
		Size: 29.8 MB (29753912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce63b63b80f8ad1f2bb7d21a4ac1212764374248811e3b88b3b35c02de53860`  
		Last Modified: Sat, 17 May 2025 08:42:43 GMT  
		Size: 54.7 MB (54716182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffad8a6351e044edf328bfeed92e84797937799e9882a15cb06250973590b718`  
		Last Modified: Tue, 13 May 2025 17:53:52 GMT  
		Size: 71.7 MB (71723837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236588b10bf795b6808ba64085740a87a27d11e2da86b3da3cac6379569a51b2`  
		Last Modified: Sat, 17 May 2025 08:42:23 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c3d41ecaeb82ab5bfd7f9a22f1b68f6ac45ca951dc81527ec527ad5e95ebc740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5202568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d73b0a47bc3542ef595a66a9a70067507e1a6e4cd34b1a60127e06764e586b7`

```dockerfile
```

-	Layers:
	-	`sha256:f016edcdfb4acde6d9bc52ba972011f5892318bfcdc2741bb3136866bc3e7d6a`  
		Last Modified: Tue, 13 May 2025 17:53:51 GMT  
		Size: 5.2 MB (5188297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ce80793f749dd21e7dd9c51176501f6ddbcd45bc38c9a5967123bb592ef9880`  
		Last Modified: Tue, 13 May 2025 17:53:50 GMT  
		Size: 14.3 KB (14271 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1530-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6d1d5730ba109df4a2ad122fb4404ed073d0e7b3224b6658ebf16df7054acbd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155607544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4468739fe9d9a04c8fc6bdde3a14c6c7dc46261c93e76657a871c54812ff6e4`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1745798400'
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
	-	`sha256:d0342bfffaba1a8be0950e44b5334c6cf9a05d9eedd81a042ec7813ac91850a4`  
		Last Modified: Thu, 08 May 2025 17:31:22 GMT  
		Size: 30.1 MB (30130233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f7d0ac33a92caa5a19b42990018d98913c7f66e7505f06fda9bb39796c5cbf`  
		Last Modified: Tue, 13 May 2025 17:54:29 GMT  
		Size: 53.8 MB (53830516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6850ffdfc6fb192c30b47d6e6071036cb676d87ac9b51a64ff2c85b3e969b5c7`  
		Last Modified: Tue, 13 May 2025 17:56:10 GMT  
		Size: 71.6 MB (71646149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b965aba53d75a73e610930478625614c573659d05a1dd57776aee3d22dda1d8`  
		Last Modified: Tue, 13 May 2025 17:56:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:97d31ac0d15c75c405d9152719cbc18bd66e60034ca89a4046fbbb4753da9158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f7113acd4b0a5ea2a3818a83513e52d46fb2c92e716fbb48e7e914fea101f6`

```dockerfile
```

-	Layers:
	-	`sha256:4ea31d9701a4543c2a965512b3cba5b011120ebd402e1ce5692c41f959bf4ce2`  
		Last Modified: Tue, 13 May 2025 17:56:07 GMT  
		Size: 5.2 MB (5194764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9671323e19edd77bcfa085ba125be6f56b0c3440236906fdb6d1dbc522579ce8`  
		Last Modified: Tue, 13 May 2025 17:56:06 GMT  
		Size: 14.4 KB (14389 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1530-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e60429e6b1cb3c21cf84d316d813f9e590327bd56bddf7b881842494bbaf5afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (162961625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09bdbb9a5d132e6cbfc6664b0aa2d841542e6f166bf2db1c5ce06be2ee381fd0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1745798400'
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
	-	`sha256:a739447e8599431e1e4996b4b6d4022822d37eddea9a3737acbea74b8a860d49`  
		Last Modified: Fri, 09 May 2025 00:17:30 GMT  
		Size: 33.6 MB (33577694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ff01908b868a75c17f94ffc5626215722b986fb8c1aeb2606b9cecf365a22f`  
		Last Modified: Tue, 13 May 2025 18:05:52 GMT  
		Size: 52.2 MB (52167960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0018011cfcd35b42fdb01b9646dfdc8ecb23442e15d2995a8f8fb9d74469db0f`  
		Last Modified: Tue, 13 May 2025 18:20:25 GMT  
		Size: 77.2 MB (77215326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e3f0ddce12cdc2805b643c486750bfc5e42e84d439105387608faa95621f7a`  
		Last Modified: Tue, 13 May 2025 18:20:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d55a97bdb7f9740d7483eb3e9aa6cfe0c56ffe0a30fad92a328b544d733a5ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5207418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff2fcc0864d8658074e1f0e97e2fd32942aa354be90e2eb49387896d8707206`

```dockerfile
```

-	Layers:
	-	`sha256:45d2d752a8a9f98f563b70e1d88250b95b67d8c9a29acc167f6a29075c7e584e`  
		Last Modified: Tue, 13 May 2025 18:20:22 GMT  
		Size: 5.2 MB (5193099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0f8ee2b63c18e3c61e22e678fbb056c3a8f0bccc3bc8924b1584f7471cb41f3`  
		Last Modified: Tue, 13 May 2025 18:20:22 GMT  
		Size: 14.3 KB (14319 bytes)  
		MIME: application/vnd.in-toto+json
