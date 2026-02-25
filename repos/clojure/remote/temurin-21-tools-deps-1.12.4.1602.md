## `clojure:temurin-21-tools-deps-1.12.4.1602`

```console
$ docker pull clojure@sha256:265816fc8601ed62d767137bb3e649739f366d2e358528ca7c5faa9531de3599
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

### `clojure:temurin-21-tools-deps-1.12.4.1602` - linux; amd64

```console
$ docker pull clojure@sha256:f0af3e6bda9da2d959e152f46184b87d18c6840140de0f002180b00c3e65f28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287497309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51b15da13476fb044936425bfef9576913abb02e9a7fb865e54613cc2d4d5ce`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:56:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:56:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:56:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:56:10 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:56:10 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:56:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:56:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:56:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:56:25 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:56:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad774665adc6e15c1b980e49cfa7d7cb7318fd9a5fbdca51eb09f508ef493dc`  
		Last Modified: Tue, 24 Feb 2026 19:56:50 GMT  
		Size: 157.9 MB (157857099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff1473eeb6f8f4c7ad4eb5e6050cad4c368724e2f3fc8248ed570884a20debd`  
		Last Modified: Tue, 24 Feb 2026 19:56:48 GMT  
		Size: 81.2 MB (81150399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2054dacaf863bc8f5435ff39072ae44d3bccac2d358151b389072bbf71b68b7`  
		Last Modified: Tue, 24 Feb 2026 19:56:45 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61dd8cfcbe3cb23ae809271029a358fad4b628c6f7f60a36475f4d7710767e09`  
		Last Modified: Tue, 24 Feb 2026 19:56:45 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602` - unknown; unknown

```console
$ docker pull clojure@sha256:82e4b7430c7e7b267ddbdf3294f8f63ce9cf7ddb937100936d8b81fa300ac48a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80521997d9aee6614b45b7650dcb579ed839777c64441a49aef0130edceb4db7`

```dockerfile
```

-	Layers:
	-	`sha256:8ecaa06b20b9a65d294504018e8ba113261194400b1296e9342bf3b6ffa7c007`  
		Last Modified: Tue, 24 Feb 2026 19:56:45 GMT  
		Size: 7.4 MB (7379325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faab0197483294fbe1829b6eb68dd846a029c58539cd23c57c13a7b2afa33e98`  
		Last Modified: Tue, 24 Feb 2026 19:56:45 GMT  
		Size: 16.5 KB (16461 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c5ab26ec3d9c302cb6811b74c830eeb76a8eabae5aac329d749d444fc1278c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.6 MB (285645865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157b6eb5c4309077f7aaaf79663b90ddaf7db87941cc1c5f559f1327a3e05d5a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:06:39 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:06:39 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:06:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:06:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:06:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:06:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:06:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c94e3358edcdd6ac1aef8c34bf7aa67e8a290a8492902766b457fb53e3d646`  
		Last Modified: Tue, 24 Feb 2026 20:07:18 GMT  
		Size: 156.1 MB (156133080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ddb37bbccba8905eecbbce6a3cf0e0ccc35984f226e59e7d1ef90b332679f16`  
		Last Modified: Tue, 24 Feb 2026 20:07:18 GMT  
		Size: 81.1 MB (81138533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb5ce58057cc57082f4980bf902d668f5b00b2db71fe2f98c4ec68b99dbdde6`  
		Last Modified: Tue, 24 Feb 2026 20:07:15 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d814278acfbfce4854ffebe946716417dbff7d90177d237e9f98cc5f109f8ae`  
		Last Modified: Tue, 24 Feb 2026 20:07:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602` - unknown; unknown

```console
$ docker pull clojure@sha256:5580caab6ddfafcdca21c6cb3626e76906b363b195ff757e93dd0110522d84dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446af2d95dc5e7cc3e79471e737729b4e4a83e87f2785c85436840e7284d4105`

```dockerfile
```

-	Layers:
	-	`sha256:8fe243d6b08a3aba52c2feade23e5435570fd5de05715c84ea59d73c6180c95a`  
		Last Modified: Tue, 24 Feb 2026 20:07:15 GMT  
		Size: 7.4 MB (7385112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4796e4608a7156d7160c9853201779df6878d56d6ab08c5ac85a5191bfc47d96`  
		Last Modified: Tue, 24 Feb 2026 20:07:15 GMT  
		Size: 16.6 KB (16604 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602` - linux; ppc64le

```console
$ docker pull clojure@sha256:cd3b43737c106b7bfade37d32c53db35d4162ebd9a8227d4a898d5211077d6dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297302462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c33feca0fb9d680ae67f15bcf8807505836fe590e2ead0113d2f82a0fd28025`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 25 Feb 2026 02:05:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 02:05:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 02:05:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 02:05:49 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 25 Feb 2026 02:05:50 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 02:10:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 25 Feb 2026 02:10:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 25 Feb 2026 02:10:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 25 Feb 2026 02:10:59 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 25 Feb 2026 02:10:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d3f5e74242b563425489fb40e572f07cd179ee7a7b86fa1a8e8f36a083f08c`  
		Last Modified: Wed, 25 Feb 2026 02:07:30 GMT  
		Size: 158.0 MB (157977502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd084a20346dc2cef47eb42b0d8df9bedc735a61e68133a87c85f49c8fe22ff`  
		Last Modified: Wed, 25 Feb 2026 02:11:46 GMT  
		Size: 87.0 MB (86987121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c74fa4c24b629bd6086968e35483158f33263998d0bd3ece95d56827a22bc65`  
		Last Modified: Wed, 25 Feb 2026 02:11:44 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1712a7290dc8f8cd3af42e2c7834a54398e276b5ec6c33da9c54ff312f7766e6`  
		Last Modified: Wed, 25 Feb 2026 02:11:44 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602` - unknown; unknown

```console
$ docker pull clojure@sha256:e0a9a2cacdb80d7ea6f19367b1e88def9ffe8ce701c43a9ae46554cbbb1875c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4cd3ad87f1667e98527e8e04d00de947a37e246e4ed696a78bc2af785e971e9`

```dockerfile
```

-	Layers:
	-	`sha256:cdcb0cca4b076c006f7c5ba88b67ef1e34818af2ea7fd6d8659a8711f57689fd`  
		Last Modified: Wed, 25 Feb 2026 02:11:44 GMT  
		Size: 7.4 MB (7384553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7cdff084b1d01f0d9d14b6a8900e8cc0d478bfe722f40df7cb708191341fe22`  
		Last Modified: Wed, 25 Feb 2026 02:11:44 GMT  
		Size: 16.5 KB (16522 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602` - linux; s390x

```console
$ docker pull clojure@sha256:f28660ff64b3523a3e65136cfffc568fadcc85589c629b9a80a1bc4f80b392ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274218092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c5e44cd3dd8a1bdc3f308195653d788be7d5456aa73ea2dae4755a06b5ca82`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 23:19:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:19:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:19:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:19:01 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 23:19:02 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:21:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 23:21:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 23:21:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 23:21:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 23:21:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49354e9f0679f3ff8b88e9d693551817e9930dd3f79f0b6470d4ff396a09d7f9`  
		Last Modified: Tue, 24 Feb 2026 23:20:16 GMT  
		Size: 147.1 MB (147105304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c639360dd0adc21d681d7ee189a45a8d0911e357391fd7aa5082080953cf3b8d`  
		Last Modified: Tue, 24 Feb 2026 23:21:55 GMT  
		Size: 80.0 MB (79963664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f76f9eeacd2319b436148748dca7d998ca405e25997f2462eb9a3f80b4526d`  
		Last Modified: Tue, 24 Feb 2026 23:21:53 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900dd9f745e431a104ce3d28455f3842b0ba0884502e3eb92f9584c1cc393d2d`  
		Last Modified: Tue, 24 Feb 2026 23:21:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602` - unknown; unknown

```console
$ docker pull clojure@sha256:4f17b844e9c300602af2e4d9840402cab8462351249abb8f3a801ed714bcfa7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7387106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2282db8ffe5dc5afffc1cf2b983f6b444edb0e210f2e648de055dce8576b26`

```dockerfile
```

-	Layers:
	-	`sha256:70c919888c4c7456a51a51c362da4956182eeeafbadc12c9dfedd9587f3e4974`  
		Last Modified: Tue, 24 Feb 2026 23:21:54 GMT  
		Size: 7.4 MB (7370644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4db58615e781ced0020791f3b1733a6dc4a8d1ac0c5e890e6aa65fa1b8efb19`  
		Last Modified: Tue, 24 Feb 2026 23:21:53 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json
