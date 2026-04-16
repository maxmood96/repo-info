## `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye-slim`

```console
$ docker pull clojure@sha256:f6cd08a30f3d7bc0cf331880797b46dbb08ebe8ea5000fb4f7f69e3976384853
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b31b1c4a9ddb0fe2564b0b018dadad41de90e2f0512af0e6dee23b1b7e6fdba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.3 MB (235257349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdf88daa41e2ace1d6edab2ed872fb750df849a92cf5f5752e85c028338e13a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:02:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:02:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:02:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:02:53 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:02:53 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:03:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:03:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:03:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6cddbd6d75ee219005cd958811fbae0fbee07d9e8c95b70331a2d6d8d0c85ed`  
		Last Modified: Wed, 15 Apr 2026 22:03:28 GMT  
		Size: 145.8 MB (145806808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee90380fd03619f88887d53d319661aee78a0a90268421faa0705cbf65e134a`  
		Last Modified: Wed, 15 Apr 2026 22:03:26 GMT  
		Size: 59.2 MB (59191876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbe85eb5ae2ac858fff0f7d510827c1b968370012b7ecc4c28d768a4cfaa48d`  
		Last Modified: Wed, 15 Apr 2026 22:03:23 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f26b9bf671c0ad2141a8f9bce40c56b3a6c8d4799e76774ad2c3d56328b81504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5354461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92fa7839a2f12d6d6cbac5c77905b660bab4cdfe535580c35f879ad1d3e3e91c`

```dockerfile
```

-	Layers:
	-	`sha256:ef3c36c7aa8a84f18d90e5c57248ffe5c4471c32c381870001002001dc641abb`  
		Last Modified: Wed, 15 Apr 2026 22:03:24 GMT  
		Size: 5.3 MB (5340194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:957d67333e6664c54e9259d47abb97293ac0f8aa857c174e8db932f22a44fba5`  
		Last Modified: Wed, 15 Apr 2026 22:03:23 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d2501c19b5989333ddeffbb5d7d69a02b9448b765345af47912bf83612d0d1a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230576461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fcaf45f37a1a20388cf3b87c37ce448e4e26990099da7453362cde9f216a51d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:14:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:14:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:14:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:14:20 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:14:20 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:14:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:14:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:14:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1ea7b02705de9c4431f4828fab0fc092d8280a64fe42c2634be6898f98390c`  
		Last Modified: Wed, 15 Apr 2026 22:15:13 GMT  
		Size: 142.5 MB (142500802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff05e83def96fc55793fd4bd606d04816d2fffe1969ab8e5a16fe4a420f0070c`  
		Last Modified: Wed, 15 Apr 2026 22:15:10 GMT  
		Size: 59.3 MB (59330326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9797ce6bc6a86f36fa88a39d49c6d47dbca84a4cd8fcd32ed92f8fa159d024f2`  
		Last Modified: Wed, 15 Apr 2026 22:14:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:df7c788396731756299061c088b69bb79a68ae0bad834145467798e181012918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fd9a30e885ea3acaa2c6efe4d3c029e16ceb86ccc1a8a257a3464431fe93ce`

```dockerfile
```

-	Layers:
	-	`sha256:c51e075c79358ecd11c90d281ca6604096d33748272afd5669d21813af2d0698`  
		Last Modified: Wed, 15 Apr 2026 22:15:01 GMT  
		Size: 5.3 MB (5346544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a314085edaff25da0d2be04797b76658c57a646e4f5b56222de95ada329f4ceb`  
		Last Modified: Wed, 15 Apr 2026 22:14:59 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json
