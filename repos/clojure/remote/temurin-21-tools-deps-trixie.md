## `clojure:temurin-21-tools-deps-trixie`

```console
$ docker pull clojure@sha256:4fedc57dee24d732cea1c4e49c63197823c6c385fc51ef2096e511a1b630b835
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

### `clojure:temurin-21-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:3abfa93645062e9177aba70d024e2de7f5f6ce0c3dd2765af53acc90ae8ac0b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290004764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7211b09584054f3d556ccd429b239ec6e76ef3bc3a6c7b02d62dc635d427a203`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:20:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:20:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:20:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:31 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:20:31 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:20:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:20:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:20:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:20:49 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:20:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aa3e9ef32f73c30e8b065800ee66429992d3bfea6a1fb8224afdd878ab5b994f`  
		Last Modified: Wed, 24 Jun 2026 00:28:33 GMT  
		Size: 49.3 MB (49317255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02630573b9f74ad2005ea8c3b3531cc756ba764e1c1cf67c9b602c00e840d5eb`  
		Last Modified: Wed, 24 Jun 2026 02:21:13 GMT  
		Size: 158.2 MB (158166915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160b59d5db273ab25840471d64accee65afa259a067f42e110b229c351ae67ec`  
		Last Modified: Wed, 24 Jun 2026 02:21:12 GMT  
		Size: 82.5 MB (82519551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df49ae55bb0c8a48d8c4a67f30f3c43f3c3f178a046e54ec822934cef1de984e`  
		Last Modified: Wed, 24 Jun 2026 02:21:09 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0fb94fea7bedd9cb3aa8911f9868dbb5cb5f1777bb7d72414d10373c19ec49`  
		Last Modified: Wed, 24 Jun 2026 02:21:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:be372e72db464cc7249ff5fab7d0e413485edd5fafd50713cac796135ea5132b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3706986703420b8215fe7149bfb3ebc31947a4c141cab59d4909f326a6986b`

```dockerfile
```

-	Layers:
	-	`sha256:69c9275f14d7a078e42fb9357ad01df06db49dbd6daad1d36f44a4cf178aae21`  
		Last Modified: Wed, 24 Jun 2026 02:21:10 GMT  
		Size: 7.5 MB (7470623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1a3f3da2a1045504bfc20b3551c2d7b3796ed107017dc3f38f16931e098392a`  
		Last Modified: Wed, 24 Jun 2026 02:21:09 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1b0663d1581ace513be34ac64a30e660784e2f4a877fe021bf17a88a2884a4a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 MB (288479177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8595393381af6c870bc91d8280bd63295f63af9dd2a1236a5e9d837d491aca08`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:27:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:27:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:27:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:27:00 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:27:00 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:27:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:27:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:27:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:27:17 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:27:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c8a311258fd162f6aa0db134045a19154c81a2244ff9ed7620256c95ae5d6b69`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 49.7 MB (49678395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681b265d72733ee19523ddc7904af3b86def35b92baa81d57f4d39027caf3c64`  
		Last Modified: Wed, 24 Jun 2026 02:27:42 GMT  
		Size: 156.5 MB (156461252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b65ec255c5d0ca2e9bb880c7d8e9441ba1848358b9ad336ba96832c3b42256`  
		Last Modified: Wed, 24 Jun 2026 02:27:41 GMT  
		Size: 82.3 MB (82338487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9cd35e8de03237d1d818d586f6487f7789fda208d0c8dbd56292791f2710a0`  
		Last Modified: Wed, 24 Jun 2026 02:27:38 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26172dd42da065021c5d88b2f7a0d26a7f0350755d0508105d43eb37cbc93806`  
		Last Modified: Wed, 24 Jun 2026 02:27:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0c5dc8f698f5651b678873896d876f6b2f917e8c28b99a7a2f74ca263d86040c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14867694662859ec38648731f9f99c7f0b8e428c6f76c1db63dba8c9dff966fd`

```dockerfile
```

-	Layers:
	-	`sha256:09a4b8e6e32d6ddf49260347ef9dabe1361d83c647aa8e02b8ac445072246381`  
		Last Modified: Wed, 24 Jun 2026 02:27:38 GMT  
		Size: 7.5 MB (7477016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb3c7eb9fc67a5dca0fe046d438bfd1c0088ed2c05adaabe66308270c9961976`  
		Last Modified: Wed, 24 Jun 2026 02:27:38 GMT  
		Size: 16.0 KB (16026 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:750a1196e143443a0faaaacdf8d1fce0b113848ba9a621bb6af4ea2a6600f556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.4 MB (299421061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee698f074190f4577124eb181e6f3026a7a2d0547479759ea63b3583ff78b14`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 08:15:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 08:15:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 08:15:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 08:15:22 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 08:15:23 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 08:21:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 08:21:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 08:21:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 08:21:20 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 08:21:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:99b7058514c1f9221ac3b0625d731341802c32d464fd604a099ae71d3765bbfd`  
		Last Modified: Wed, 24 Jun 2026 00:30:31 GMT  
		Size: 53.1 MB (53138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8411e185f9b4e8882a4fcb58a6e9dae45b9847e5c95ef274b2a91a371cdf3a7d`  
		Last Modified: Wed, 24 Jun 2026 08:18:58 GMT  
		Size: 158.3 MB (158343230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ba9e6b98cf2c824f53d19e8df1c77b3b4125745c22a8383c70b6191e92be81`  
		Last Modified: Wed, 24 Jun 2026 08:21:59 GMT  
		Size: 87.9 MB (87938724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9672759fadcb35ab2c8f86624f1d73ee4a3861ed008090e907cd1ac2566d3efd`  
		Last Modified: Wed, 24 Jun 2026 08:21:57 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f0bcea98157f320f5ac1c645a4668f8073fdfd7c9b5706a6000333915e41ca`  
		Last Modified: Wed, 24 Jun 2026 08:21:57 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8b6b494ebc5d78e942846259aa1f6e710711ea7764f35ae5ca813d78c09ce9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1654097a7beb0e4619e49de7b5520a331c8ed0cf17ec1d68c28afeb8d3ef3ae`

```dockerfile
```

-	Layers:
	-	`sha256:ae045913d4e0eb7e7ee9bfd716d4f801856bdd834c5c8dcce0d2c8aae3db7264`  
		Last Modified: Wed, 24 Jun 2026 08:21:57 GMT  
		Size: 7.5 MB (7475044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a879057f861f8d237a282bdf4053be141c4c84b20b2984ba22e1f850b0e2b52`  
		Last Modified: Wed, 24 Jun 2026 08:21:57 GMT  
		Size: 16.0 KB (15956 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:7d4fd4927a8c4011ebb3b30942f15f2380ba80079698c9b8c28340760b28ae6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.3 MB (280277285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470d77960fe936020ef221cf311f4a9642ec5588658cb7bd2425324af2d1bf07`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 04:14:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:14:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:14:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:14:44 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 04:14:44 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:16:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 04:16:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 04:16:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 04:16:53 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 04:16:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4acbf08d84aa74ba1f41a222ae6a061c228f6ba4fc5d1d428650c7427ca1fbd3`  
		Last Modified: Wed, 24 Jun 2026 00:28:42 GMT  
		Size: 49.4 MB (49386060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1502a35598bf9e3752b337faf32f27269073fc676e3ffc1946e8526c29cc1a58`  
		Last Modified: Wed, 24 Jun 2026 04:16:19 GMT  
		Size: 147.4 MB (147388359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b81e298c6b9a60100dbd21bec9c2b1bfb69f934a6e8c518568ece84dca6a85`  
		Last Modified: Wed, 24 Jun 2026 04:17:21 GMT  
		Size: 83.5 MB (83501828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464cacfcb0d89310916a6fb702f36af1dc059c7bf3f4a2f7b35486eb8a9c407a`  
		Last Modified: Wed, 24 Jun 2026 04:17:18 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd50ff423e27e89a0e4bea3d9825c56fd340ba2a10463c4c1af297271adeddb`  
		Last Modified: Wed, 24 Jun 2026 04:17:18 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:036ff6d86baaa172e49eac80e1b5ae6e627c618f197e4d57d38a5d6cff9b7ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e5a93800f7c0f65f358b30c7a2918d44645e0b4e303b0015c85d9d01690b5d`

```dockerfile
```

-	Layers:
	-	`sha256:5535f00a58fad865ac5d43a59769817afef7615d8cbb70193c435e2045b7f298`  
		Last Modified: Wed, 24 Jun 2026 04:17:18 GMT  
		Size: 7.5 MB (7466545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:442770c72dcb1149d881e7873ad1c3657a397d9df37ab6668dd547bbbaab7759`  
		Last Modified: Wed, 24 Jun 2026 04:17:18 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json
