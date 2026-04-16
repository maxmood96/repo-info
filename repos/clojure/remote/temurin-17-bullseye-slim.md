## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:88e70e2174a05b3c6a88a4af2671565db02aadb30642e3da614b6bbdde687955
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:65358747e9342b34ea9caad1247eebea29905681ff99728bf3144ffb490470bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235079992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7651b8c288dbc7d8395e94f5ece01cb5837db0af7a58f8c72eca71fdb5ddd42a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:04:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:04:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:04:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:04:23 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:04:23 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:04:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:04:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:04:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:04:36 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:04:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6faf79026f6babd44b04dd5887986383cd0cbba011db172ef5114940c456ac0`  
		Last Modified: Wed, 15 Apr 2026 22:05:00 GMT  
		Size: 145.6 MB (145628776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf2fdd4538c728b87790a0b2d222c4a4b0d485cd24d11b1492ee1ba394644ab`  
		Last Modified: Wed, 15 Apr 2026 22:04:57 GMT  
		Size: 59.2 MB (59192155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e500d194476571f5ca11b99c8e4ca32aa808b3a6d25d420e764d7421974a2cd`  
		Last Modified: Wed, 15 Apr 2026 22:04:53 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5869097a110b105557117954fb21e821014e04be333db0c15c023ed4aa17908c`  
		Last Modified: Wed, 15 Apr 2026 22:04:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6caac81f94cef8deb4f78f807c27ea69bf556f70ac36932194ed4ea4aac601dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5335887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9932e5d5760c6277b0721b2e526f26331529b9f4e9b8e0bd30ffabc47a0482dd`

```dockerfile
```

-	Layers:
	-	`sha256:57e2c324713c12f161e89bc0bc2a8e6161293cc259b7725c2c264773cdf49c6d`  
		Last Modified: Wed, 15 Apr 2026 22:04:54 GMT  
		Size: 5.3 MB (5320053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3db656961f850861741682055e87940137f38efd4d866a75e9951aecc5b35dcc`  
		Last Modified: Wed, 15 Apr 2026 22:04:53 GMT  
		Size: 15.8 KB (15834 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:22fc7a366df9b59b7e280b2a36cc3cd22cb95e005d240b08c740474602204c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232505666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9e84e62a3df4d8d2dca12d87c52896df8b9e4f5432e0ad0d17ae4032f55aa2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:25:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:25:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:25:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:25:58 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:25:58 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:26:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:26:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:26:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:26:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:26:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d6c4fc109c3b8daa3acd20f621fc415c4da4df34b15e2c82dffe5f3d189c2f`  
		Last Modified: Tue, 07 Apr 2026 03:26:37 GMT  
		Size: 144.4 MB (144436221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c57b53d049c86c0cb29df2d51f5451d9a76cc837f47c2b5c16d713aedf2b3c5`  
		Last Modified: Tue, 07 Apr 2026 03:26:36 GMT  
		Size: 59.3 MB (59323715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920de38886632317f5933dd446809f18cd7205e5fc677781e25e11ccffb05bb4`  
		Last Modified: Tue, 07 Apr 2026 03:26:33 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ff3ddd136144f08d338e53d9971ec6c4bd560c2d7ba0ac3fdd5bb16be04b9a`  
		Last Modified: Tue, 07 Apr 2026 03:26:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7febe69e68589e15f8cfa782c44fecd71e833da4905bb4a30847a590788e888d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5341739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6795d1bb92352b02233ed66dc9a7d097becb24b1d1bf4518f704e264bdf8cac`

```dockerfile
```

-	Layers:
	-	`sha256:66a3c1a45fb41a12493c369faf0926007f2ea528af329ec7ec8c3cd1f11c86cb`  
		Last Modified: Tue, 07 Apr 2026 03:26:33 GMT  
		Size: 5.3 MB (5325785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0010edb4f2155c8731dba65e1a5c26941ad66e1ec2d9935f9c4bb6edba263f01`  
		Last Modified: Tue, 07 Apr 2026 03:26:33 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
