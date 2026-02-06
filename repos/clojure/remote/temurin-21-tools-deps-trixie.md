## `clojure:temurin-21-tools-deps-trixie`

```console
$ docker pull clojure@sha256:59d9ccafbb052bf07200149f6e3df37b31ac536f1f2d8cfff18981603ed5740a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:eff65bab54832bfd92134874358e7c10664b0e6683fa91551fa47f74ddc77fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292693396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0b3df6b4a438c0b09eef3e7e2e03b5e84d7634c61feb08711f2dfa18443014`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:06:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:06:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:06:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:06:25 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:06:25 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:06:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:06:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:06:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:06:43 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:06:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b413f1fe645e05e134003ee96dd924d1dc7be58374b435d1e81119bf6c8fec`  
		Last Modified: Thu, 05 Feb 2026 23:07:07 GMT  
		Size: 157.9 MB (157857074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e0587e96fe2bedc852882c81ee532de2779f7ec1cb572c76b2fea9a72b0792`  
		Last Modified: Thu, 05 Feb 2026 23:07:05 GMT  
		Size: 85.5 MB (85542330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17c5936ec0e40de5e6657a5d8c71d38ad0cbfb2cf1ef871819f8257d9120894`  
		Last Modified: Thu, 05 Feb 2026 23:07:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb3da12a1c3a2ef5050c692092c85ab69415dd3f6200502c99d95c74164d42e`  
		Last Modified: Thu, 05 Feb 2026 23:07:02 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3ecd2cd0d33b2299e250549192fb45cbfc3c01e02f9078457faf3a2864d4afb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03703c82feabad093e72c1a526d7f13069743e758479c79822bcc172cb8b4d88`

```dockerfile
```

-	Layers:
	-	`sha256:758d65263126b9d522b712e32adf662e592fb87a0120fe7019587b4ae9011b21`  
		Last Modified: Thu, 05 Feb 2026 23:07:02 GMT  
		Size: 7.5 MB (7470932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14128e4aa734fafeeb32cea988216557c441bfb3cbd1c1b8e42bd17b989bfbb6`  
		Last Modified: Thu, 05 Feb 2026 23:07:02 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1751c87324066ea22385c5a851f23d99130fa68f061747b7b952c7bba4cd5c1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291146886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3cbf1fccb315f94ebac8aea007f1983cc2a603e2f701f0e98847cf5af85a42`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:07:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:07:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:07:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:07:23 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:07:23 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:07:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:07:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:07:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:07:41 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:07:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9c5c3fd71b028ef3e7439c4f837adfa814089a9bb1e1808c619a80284cdd2f`  
		Last Modified: Thu, 05 Feb 2026 23:08:08 GMT  
		Size: 156.1 MB (156133068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15af8024aa7d3e0635f08596987ab0ee0839c1b5f41d5e856091b99fa66d322d`  
		Last Modified: Thu, 05 Feb 2026 23:08:06 GMT  
		Size: 85.4 MB (85360758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b902c5ac33d89100a4cda2a3c057e761620578a10ec425922fd80d885e6446ac`  
		Last Modified: Thu, 05 Feb 2026 23:08:03 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628eda5b90fd9e337043c8651dae2cf4e7dfb9abb71fc173924dc09ee25678c9`  
		Last Modified: Thu, 05 Feb 2026 23:08:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fbc346bcf1dbfa7d3396519ad6e4e564f847e2b1bd536ae28e7167f98a2bd306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d64d9cff5ba44561c94b7bd3bbd1b445ce473259821f25b6607935821c5eeb7`

```dockerfile
```

-	Layers:
	-	`sha256:c4c9600ea201686ba6d8afd299d5e5f4013b80f91dbfd87f46bbff8cda7b8b59`  
		Last Modified: Thu, 05 Feb 2026 23:08:03 GMT  
		Size: 7.5 MB (7477962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c1d1af3b99961dc55c77c54263b65cd2035d3fb41ca7883632e88775fb81728`  
		Last Modified: Thu, 05 Feb 2026 23:08:03 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:f41b8d77a91ae31b54278f63d0bd7bc71c7e980320a2c55ee1aa19c6da9efb07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (302038027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82a57bea12cbdba22ad9eebc6883858057284b7d95aa352a5ced68173dd5ff3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Fri, 06 Feb 2026 00:37:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:37:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:37:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:37:54 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:37:56 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:44:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:45:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:45:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:45:07 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:45:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d803d46010c6f6fae7ea82f881a836bc9d2bf4afad631cfb7ffd52616e4eec`  
		Last Modified: Fri, 06 Feb 2026 00:39:44 GMT  
		Size: 158.0 MB (157977492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658dc509fba83dc2db068bc8e8fc1b00a423baa6138f80c8f6e1ef787c8cc2a1`  
		Last Modified: Fri, 06 Feb 2026 00:45:56 GMT  
		Size: 90.9 MB (90947375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b57375455d750ea82383acda1d01ccb215922e56b701bcee8390cb6e0bb6555a`  
		Last Modified: Fri, 06 Feb 2026 00:45:53 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d14c407954658464ba427b45e5d4df4f7bfb10593481a4ecd3e42d9773d07ca`  
		Last Modified: Fri, 06 Feb 2026 00:45:48 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:074e5dd2ff473ea20985643fd489e072a05aacfebdb17042c0861915dc0c7585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0073d843ad9f75c881818998ad747306d824dd70dca259705fc3d86c7043301e`

```dockerfile
```

-	Layers:
	-	`sha256:500590ae1ab198493f54aea2338d28f244f1b8a5e7d912d8151ae7c697f3c02b`  
		Last Modified: Fri, 06 Feb 2026 00:45:53 GMT  
		Size: 7.5 MB (7475353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa4f45732bc24240c69f1e2efbdfd384c216bb5df19d08ca2a8bd468faf905ea`  
		Last Modified: Fri, 06 Feb 2026 00:45:53 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:a3b1349369688d4a02babdeeac586ad906945e08f2f5924b021c3c0088557e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289397267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a9ab2375fc9260d0bf68c08c57ab9297280cca78546e193d2165385228be97`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 20:42:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 20:42:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 20:42:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 20:42:20 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 20:42:20 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 20:59:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 21:00:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 21:00:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 21:00:00 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 21:00:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:618efd37f74728f7dcba60c231fad7f2d777dc65e4da32d0adae5e032e1fd125`  
		Last Modified: Tue, 03 Feb 2026 07:13:10 GMT  
		Size: 47.8 MB (47776763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1cdbd3dbc058f023650ab2a7a190ceae0ea518397c9e3b43d69e110a89004f`  
		Last Modified: Thu, 05 Feb 2026 20:49:34 GMT  
		Size: 157.2 MB (157194298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe37afcdc3897f84755539a458de2d10bb7bce0ab1cc84dd101fbab8f707ffd`  
		Last Modified: Thu, 05 Feb 2026 21:04:36 GMT  
		Size: 84.4 MB (84425161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7843c43296650414f924034a9e09794547b11606f6dd4e10ee77ee4f7f2b37e0`  
		Last Modified: Thu, 05 Feb 2026 21:04:23 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca921e30660362564f1ebe2dd1012071925a132865625b5769849a2a79353754`  
		Last Modified: Thu, 05 Feb 2026 21:04:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d0e2b4bfccc5ee262f40aee607982f7f7e479b649aae786f04bddfb64e0e972d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7474647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abab08bac1a1ea5057b0b41fecbc3f383c3dff62697df67af74d277a143174ab`

```dockerfile
```

-	Layers:
	-	`sha256:c89d80b0824f03441ea567054ca1feb5432fc893a4d111127f91560cf21e71b8`  
		Last Modified: Thu, 05 Feb 2026 21:04:25 GMT  
		Size: 7.5 MB (7458845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:303d6cabfd44c2f7d2e33ce5fbeb2f779b7da8081cf7e2eba37b9a1e081583c7`  
		Last Modified: Thu, 05 Feb 2026 21:04:23 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:e1388a5294bdcef24b6e288882113c155aeb29f02640b1bbc39242df009abb26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282972292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f612c5eb1bc172a7b78b0d91b00234f15cb51e39e94fc5fdc5eddda507f4162`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:07:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:07:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:07:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:07:47 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:07:47 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:08:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:08:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:08:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:08:05 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:08:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb321abad7ee48a39f052188ed9343d31c396580e281708d3c20e554f68e0326`  
		Last Modified: Thu, 05 Feb 2026 23:08:40 GMT  
		Size: 147.1 MB (147105286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6dee3531b5328fa70c3b1dbe9d3232deb687009f8963371cbf97bb81d32ab5`  
		Last Modified: Thu, 05 Feb 2026 23:08:39 GMT  
		Size: 86.5 MB (86511584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fc22d7b832c03539e1f6b90377a7d50c65abeb51434141ce54b55006044f18`  
		Last Modified: Thu, 05 Feb 2026 23:08:35 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b6cc5bc7cfa7d0f8d186d0671683ada2b0d159fc4837a677ffd533735ef5aa`  
		Last Modified: Thu, 05 Feb 2026 23:08:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3a441fef6d2152073a9e6e14fb776086b90c294e66d3171382c17800bd96244d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:961125cf08f1e8297bf7f8e8fd64b1bb12be655f8fdf0e21902b49091b79510d`

```dockerfile
```

-	Layers:
	-	`sha256:76c78c4d727648ce65259914edbf642a5a05f99144cde6e334d0c6e30b6e0adc`  
		Last Modified: Thu, 05 Feb 2026 23:08:36 GMT  
		Size: 7.5 MB (7466854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0af42746d802dec02dcfe56800098510140c8458e1d37dc9e9b3875177998500`  
		Last Modified: Thu, 05 Feb 2026 23:08:35 GMT  
		Size: 15.8 KB (15753 bytes)  
		MIME: application/vnd.in-toto+json
