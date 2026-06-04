## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:38904e11bbe0908fbcde753bf0330b6c77d3b4908d1333edc812bd001e3bcbe4
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

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:54cd8dad2dc807d400826e3352f48f2442a1b26aed9479fcb94c8d6d516b39f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240781813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471876fd1d443a08ca99750a665b565a940bed2fe82051cc0f57ba329d857657`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:45:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:45:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:45:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:45:53 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:45:53 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:46:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:46:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:46:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:46:06 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:46:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732a990a504fa55bc6fb3281aee0381dd25f8e7d2d00eaca0d1a4436d96ae961`  
		Last Modified: Thu, 04 Jun 2026 17:46:29 GMT  
		Size: 145.9 MB (145905454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb23b9f8ee59c6ff606a45db4ee4e1a9948bb68c68c7f5af7e1bfc7ecf5fdc1`  
		Last Modified: Thu, 04 Jun 2026 17:46:27 GMT  
		Size: 66.6 MB (66641769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf36b76758714165e1d9c48bfe6ded593e09905eb190dbbb03a3b6d74fb97e0a`  
		Last Modified: Thu, 04 Jun 2026 17:46:23 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99b8c5107681d29dd200069b75c48a7e87bb19566620d35b6a42194fc4a3e4c`  
		Last Modified: Thu, 04 Jun 2026 17:46:23 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:22517b10abfb38b946faaf366397f68c7ec515dd5a56fe7314635d09b56f9955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5129970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f84c74718b703305354d1552e9099b7480438cd36b09eff11e67bb488fcd0a`

```dockerfile
```

-	Layers:
	-	`sha256:0834896653cceb9f6b70a847a86c5db43b1da9c09027974337c09bc6183d3be4`  
		Last Modified: Thu, 04 Jun 2026 17:46:24 GMT  
		Size: 5.1 MB (5113981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:238657e8aba4d76221e86caf2461d345e12234150c34a6c8f9177830f8f7f5d5`  
		Last Modified: Thu, 04 Jun 2026 17:46:23 GMT  
		Size: 16.0 KB (15989 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ac6adbeadbc308a18d4860e89c187e85fef84870240629a4d00caafced3db515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 MB (239484084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e997f5ab383218bb3937ded16645d2343c34788a1a5b05164a91719d003a904a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:45:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:45:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:45:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:45:38 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:45:38 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:45:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:45:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:45:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:45:52 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:45:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81b6fa02450db45b86a4c221f3f2c217ce7097acf736364d60fdba0e42069d2`  
		Last Modified: Thu, 04 Jun 2026 17:46:15 GMT  
		Size: 144.7 MB (144724358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19eac8fe0096eee7875dcc0cc582deed6c8e4aea883c1cf814e1a1ea7b8a76cb`  
		Last Modified: Thu, 04 Jun 2026 17:46:14 GMT  
		Size: 66.6 MB (66643639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2190502c49bad7484d8d0cd1a3907b22843f2a429a900175f181c8fb33b1eccf`  
		Last Modified: Thu, 04 Jun 2026 17:46:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534042b02c74766fc829968c37d429ff87a92446048d8d609673491a3daaa231`  
		Last Modified: Thu, 04 Jun 2026 17:46:11 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c2cf563ca0735c7edd9cba1fa5b0c40b91ef9ef74c0ddd642efac2608afba23d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79ab87f773023a744561315d72abcec5b9fa3389798837f1c4f9c204565378e5`

```dockerfile
```

-	Layers:
	-	`sha256:e4347390e5aa07079340029497b81a61d21c969cc9472e14cdd0d1c368b4d929`  
		Last Modified: Thu, 04 Jun 2026 17:46:11 GMT  
		Size: 5.1 MB (5119742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa53dc7302c4c91fbada56b8557100c1344416d04e0fb5dea55bc77fd53564cb`  
		Last Modified: Thu, 04 Jun 2026 17:46:10 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ef91013dd2dee6f90fbb84377ff6de1010405cd89b5c2da36b75c601a18a0f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250318822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e97b3167fe34e828f77ec67fd63ab5c80c231617880f08cc34a9263ad7f31b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:52:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:52:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:52:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:52:34 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:52:35 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:53:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:53:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:53:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:53:13 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:53:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b07c7365abbdf51207d4fb0dce1aa01a3779dcbb02f429090ef6f23b6fd8e6f`  
		Last Modified: Thu, 04 Jun 2026 17:54:00 GMT  
		Size: 145.8 MB (145766093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b9d44e15ddcea031e922392906b467af2316659beab5dbd283b81ee9b4775d`  
		Last Modified: Thu, 04 Jun 2026 17:53:58 GMT  
		Size: 72.5 MB (72475942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4874e0408217e3bdb93b3bd597904a77171e21325946bd98d06df000aa8b9f`  
		Last Modified: Thu, 04 Jun 2026 17:53:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d4150f58a041c6f914f71f19f835fff327f8bd575d9166b7570395f9e94c0e`  
		Last Modified: Thu, 04 Jun 2026 17:53:55 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8ec59defef085624f257d88366738d966a50a52a64b2135b0307ba5067f1f864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3432313e159a074d4cfe10af0a982c2018e4f532d0fc7bbc5e0821d1883d1ca3`

```dockerfile
```

-	Layers:
	-	`sha256:744406d54e494f65188107e8efb5f99f6127c20aa0843d310f45d721505d3965`  
		Last Modified: Thu, 04 Jun 2026 17:53:55 GMT  
		Size: 5.1 MB (5119139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e89bcebc04b20334dfecb46ea6bc5933b37e9e6dc890ab3d19ac51374e5767b4`  
		Last Modified: Thu, 04 Jun 2026 17:53:55 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:9a9172b469c864dbb3540ec7028bebe042b057c330e81ac3565c44d4bb20b386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228252258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0784adfb505f7442d559d117f7cd2e73232d2883c6d3f868fc8028ffe00a73`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:42:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:42:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:42:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:42:11 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:42:11 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:42:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:42:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:42:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:42:25 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:42:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5b2bfdb09b0277d26e94cae7756f1f3dd26d911295a5535e4173b2dce8daf3`  
		Last Modified: Thu, 04 Jun 2026 17:42:53 GMT  
		Size: 135.9 MB (135910381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0930d0dbfdd0af5e19292d123905b07e891e4207d8716872a3864a87c4dbd594`  
		Last Modified: Thu, 04 Jun 2026 17:42:52 GMT  
		Size: 65.5 MB (65452237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4333c1908401915b65485d3d0021f161e39c37022d2ddeaf899085c54fd05a`  
		Last Modified: Thu, 04 Jun 2026 17:42:50 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21164dd9ddd3896dcd91776aa3e549363a9140dcdbcd2873bb11fb5ab61dbabe`  
		Last Modified: Thu, 04 Jun 2026 17:42:50 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e0dc0ea479123945131f790702de6d754455f2c70cef3dd99bdbeb89bd9eecfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5121292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe88dc8ff324c0c95fe9a5090ae441e1fdb696aa03c05f24c28dcfe30d42a87c`

```dockerfile
```

-	Layers:
	-	`sha256:b8ec61be463db3103fdd7419f8c36d3000357d816baacf5fe3648e5dfb317924`  
		Last Modified: Thu, 04 Jun 2026 17:42:50 GMT  
		Size: 5.1 MB (5105302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf98037a05cddcd4ace7b3cb0c3ffa35c1a34127fba633e574ac0d8a906dabef`  
		Last Modified: Thu, 04 Jun 2026 17:42:50 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json
