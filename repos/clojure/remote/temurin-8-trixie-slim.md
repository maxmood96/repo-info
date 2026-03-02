## `clojure:temurin-8-trixie-slim`

```console
$ docker pull clojure@sha256:b17c784a4e6c465640bee081b0f7d130baf84df18ddb51b4cf3ddedef5a829c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3ca2719c747cb653017a3ac6b96b0e62164a0e7c5a336cc5b9ee53340849e972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (156956912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80dded978b78e4a8642d9ff0f88ba13becf14fb9d3ffcff9b3df0cb04c9aa1c5`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:45:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:45:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:45:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:45:41 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:45:41 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:45:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:45:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:45:59 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8355b20e59fd16074f14198ae6815bbbdee50035018a8c2ce8ff7d31c6a73449`  
		Last Modified: Mon, 02 Mar 2026 19:46:16 GMT  
		Size: 55.2 MB (55170060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b50cbdd64e612542bd0a222ff9a617f9db6bc666a1d04e539b1bd76a31196e`  
		Last Modified: Mon, 02 Mar 2026 19:46:17 GMT  
		Size: 72.0 MB (72007576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3fa67a042576f73ff57f70ea8dd32922f40fb62b01652c9a0554edb4b92694`  
		Last Modified: Mon, 02 Mar 2026 19:46:14 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9b0859a490facce9262c3387ef331ad08040584691d80d500567f23209fc3821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5394277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0a8d2515ad8ee71c209734356e2fd44c0d3f3000c266548afdefdc39115b98`

```dockerfile
```

-	Layers:
	-	`sha256:803ba9043601129d90e112091afdf380765ae3afc0b6cc1a67e267eccf15e101`  
		Last Modified: Mon, 02 Mar 2026 19:46:14 GMT  
		Size: 5.4 MB (5380051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c61220b91a2a52cd07657556ef40abc9835875e6185e86f0bcf245c3f8fc9a2`  
		Last Modified: Mon, 02 Mar 2026 19:46:14 GMT  
		Size: 14.2 KB (14226 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c4531260108c4a402cee63af08814dc95b9a9917242310c3be5762e48a48db53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156216446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:109d40e5ce0f0e4570bc562cb6a7487ee622178864e20d3581656236b5d857d6`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:45:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:45:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:45:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:45:55 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:45:55 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:46:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:46:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:46:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70fb12541bdcb7ad7d13545ed1efc8df3f1a20e7555d164a411d43c5c0361f5c`  
		Last Modified: Mon, 02 Mar 2026 19:48:36 GMT  
		Size: 54.3 MB (54251614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178e57f199cb70213ebd6ff59085502ffbe0a33562beb6670cecd74c93933d77`  
		Last Modified: Mon, 02 Mar 2026 19:48:40 GMT  
		Size: 71.8 MB (71824089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89c90848667195693fa99318e0f649cfbc95ae454f093fafd960bfc8618984e`  
		Last Modified: Mon, 02 Mar 2026 19:46:34 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4e7831ed8f199d5b32bfc4ff89a31c43796efc2aff113354ddcc042fcf7d6de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5400866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ee02a5dd8cfea7f276a217ae988d5bc524c5208838c07cb316013a2bc06353`

```dockerfile
```

-	Layers:
	-	`sha256:bde647d73d8adcfee5b6759294cdde91f302b7c3148dd9dc50743c92e76d0cda`  
		Last Modified: Mon, 02 Mar 2026 19:46:43 GMT  
		Size: 5.4 MB (5386520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:711b2cf19b7f7428890bae050e7d4cd715d89c85188f0a16bcc3fb0b4f46b423`  
		Last Modified: Mon, 02 Mar 2026 19:46:29 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:bd2be5437f5ecc2afe6c1203e2461ea7619fee7358c95516650c912769ed2e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163669860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174db1d36ade476aea50dd3b4af9399a83010448293cbd48b3342790386ff33b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:49:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:49:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:49:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:49:15 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:49:17 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:50:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:50:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:50:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd5337e7efec536218c9c16451cace203af3101ab51ca4e2b3c94cbc6695c19`  
		Last Modified: Mon, 02 Mar 2026 19:50:53 GMT  
		Size: 52.7 MB (52650381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c327a58cc93accb967c7c85e654981abd6ad7b1ba4c62b5512da163e6c01c80`  
		Last Modified: Mon, 02 Mar 2026 19:50:54 GMT  
		Size: 77.4 MB (77418616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf2880a2d71456a5dda0b8fed903b6900ae5368390c6349b398fdfff280a0d4`  
		Last Modified: Mon, 02 Mar 2026 19:50:51 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c9d665632bd9d0562f178e61368a15f6136d35ab212a720fc4146371a66c7289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5399293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087ce36781affb132d610dd2184f4d756fae749e91908abbe9b26e3e626bfb69`

```dockerfile
```

-	Layers:
	-	`sha256:f08e7bfef380f73b7beae21870df67c022f960e29875b6ff34a07581b11e1fd4`  
		Last Modified: Mon, 02 Mar 2026 19:50:51 GMT  
		Size: 5.4 MB (5385017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14ce885618a2c3ff81e2fb433a4091dade7eab4a342c17894a05fd84ee34d8ef`  
		Last Modified: Mon, 02 Mar 2026 19:50:50 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json
