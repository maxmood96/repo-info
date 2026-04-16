## `clojure:temurin-17-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:cc03a11253bc04c0f2849e2738860e49dbb7dbe6e0f23c172ae4b5683f81194f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; amd64

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

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:980695ae8fa4f33d50ea7f6ed7a1f0b68990f2e165c09eabf049a964832a2f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232512058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa30adf69913114b09012f63c2bae0335d091194f42c2c92935d9ef5ecf7f5a8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:15:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:15:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:15:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:15:36 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:15:36 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:15:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:15:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:15:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:15:49 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:15:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7522a16a12e39e13c2d725fd9cbe7381112c625d1eb0c36fe414704d665bdd18`  
		Last Modified: Wed, 15 Apr 2026 22:16:14 GMT  
		Size: 144.4 MB (144436242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd27c30b2c4024fc4eccdccc53a486bab30a72554177c3a636db7f22f333c5a6`  
		Last Modified: Wed, 15 Apr 2026 22:16:11 GMT  
		Size: 59.3 MB (59330087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1257ee6955fd874bf2a44df0d1b7a345fbee2fec1efba846cb6f3683be512f96`  
		Last Modified: Wed, 15 Apr 2026 22:16:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050dcd409b8e5646e760c1d7279b365d20898be870744fa17209963185ec4181`  
		Last Modified: Wed, 15 Apr 2026 22:16:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:48de24cf14038ea5f68779607f606585cfa9a25c3f1cdf5e10af8baa1945cff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5341738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec6174c7f59b1a72f067e3df7a5ae7308013b723823d2f18e6e6c838728acc6`

```dockerfile
```

-	Layers:
	-	`sha256:ab7feb5baed394b89cdf64f0419c2f72d00cbf2130a96cc41c7e3f137514abd4`  
		Last Modified: Wed, 15 Apr 2026 22:16:08 GMT  
		Size: 5.3 MB (5325785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bdd68d2c713ab2a138ef065be295cc0c00b09a157306e26dd52c7fad1bc1264`  
		Last Modified: Wed, 15 Apr 2026 22:16:08 GMT  
		Size: 16.0 KB (15953 bytes)  
		MIME: application/vnd.in-toto+json
