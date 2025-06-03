## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:6f85617baea23af9d29cde2660e57d512cac1bcb8648329b690cffe6c4ba5289
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:735d9685ff69b0a45ad0fb79f1c928154cb4e1c5c7a97a983f9445294721f548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184199831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a275d9829fc26255e28701de74db30932cc5697941b2261c58b7ba50691263e8`
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
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3133d02397dddc5d5f0e5f3fb57c75c03efc7789878da92644e9acce1bcc5ec2`  
		Last Modified: Tue, 03 Jun 2025 05:15:21 GMT  
		Size: 54.7 MB (54716149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af896af86ac59d470fce326ebf0de615741d82807d40cd4875f7eacb08be3fc5`  
		Last Modified: Tue, 03 Jun 2025 05:15:21 GMT  
		Size: 81.0 MB (80994793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249bb164add4a7f5248e8799d3ef5a15152cb0f791024bd385abf2913d57aeb2`  
		Last Modified: Tue, 03 Jun 2025 05:15:20 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:91c098e646ec8a623eb747806b61d083b799a9027e1e10b3b7e317b560b8bab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7354369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc83887af73029b2d82fcccf9eac499ea0f26d75d59378cb1d4a8f9c8de876b9`

```dockerfile
```

-	Layers:
	-	`sha256:ee0cf4cbc8f2efab95cbb91f647a1cfcc1bf397f97fa374190f534274af9b2ae`  
		Last Modified: Tue, 03 Jun 2025 05:15:20 GMT  
		Size: 7.3 MB (7340132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2845f92e47d42651229792d95ff252b1b44d53bc863df1962440fbea360e54f4`  
		Last Modified: Tue, 03 Jun 2025 05:15:20 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7e9aace54766c0a16f1577dd22589217c06b0dbee70977450cb95e29e5953f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (183005147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b7c298612a1bcf9449929e2524428660d4c6b0e07dc892383cb32ce8f0349a`
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
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd4992357ba318e5480f8b56ec256a277c565a89898891e78871d47ce9c0350`  
		Last Modified: Tue, 03 Jun 2025 10:27:20 GMT  
		Size: 53.8 MB (53830497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2301502f5ea6cb0b99b6b83954616401e32f49dea486113bffa07c64bdaa3fb2`  
		Last Modified: Tue, 03 Jun 2025 10:34:13 GMT  
		Size: 80.8 MB (80846823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94427d40017952933af29778754bcfa36200883936293ea2f6387b67615918ca`  
		Last Modified: Tue, 03 Jun 2025 10:34:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:85e7dff9a06c8498a4905e9c2dc1e8832eea0133907443a55a51dca30c297a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7360948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395fa3ec085ed6f296799418c8333943add44d93da24bf204f7850631a589521`

```dockerfile
```

-	Layers:
	-	`sha256:11ae127cd1d93ef354aa1139b4a817dd836feadb11b43c6861e0db7354c02074`  
		Last Modified: Tue, 03 Jun 2025 10:34:11 GMT  
		Size: 7.3 MB (7346593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d444874744fa719d6c05604e8da4fe9a1b5e13954555c49388dcc01ad5fd9bd6`  
		Last Modified: Tue, 03 Jun 2025 10:34:11 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:bd3b8ecd2d687c8fa0146d4028829b15b4b87d27bb0cb268983787af4252253e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191310851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e200f08443fa38b63aba00adf162a5294840477828c2300d96677df0ee3d6c2`
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
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5db02309f6380af00f3a055d44f88afac6c886fbdca776378625bc23fbf4af`  
		Last Modified: Tue, 03 Jun 2025 08:03:11 GMT  
		Size: 52.2 MB (52167966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7edb5f27a1c03a5f4edcbf79ee540323f7b48ebfdb7ebf8fdc1755d9f134c766`  
		Last Modified: Tue, 03 Jun 2025 08:14:45 GMT  
		Size: 86.8 MB (86810622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cffe938579ded0572199005ebd6d8da688e7e1e8f4e98acb51ebe13dd83baf1`  
		Last Modified: Tue, 03 Jun 2025 08:14:42 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:79c3ad567734d143caefee696a66ad736197314bc6e376df3f3a07d24446c79d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7360213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a056f1f956ea8b139e46cd9b50387026f43de4fda4b358400ce4247212a3963a`

```dockerfile
```

-	Layers:
	-	`sha256:466c422981392378cf1369f8c8fb973115732d0f8c9f84c7a39e75e77a6cd089`  
		Last Modified: Tue, 03 Jun 2025 08:14:43 GMT  
		Size: 7.3 MB (7345929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78c2ae9de3640efdba1e1be860542618fb32c9aef231f2303199426a4a13b77f`  
		Last Modified: Tue, 03 Jun 2025 08:14:42 GMT  
		Size: 14.3 KB (14284 bytes)  
		MIME: application/vnd.in-toto+json
