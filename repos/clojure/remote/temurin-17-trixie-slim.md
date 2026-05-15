## `clojure:temurin-17-trixie-slim`

```console
$ docker pull clojure@sha256:618b8897cb2ed7e837fa421c5b40744144eedbf5db08c75326a07c77048babe5
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

### `clojure:temurin-17-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6222455b1c2b3f87dcd5a3657da5f5b96485dd32e5c9519e6178d033dfa8dbf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247733350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7daa32d2e4cbd50be9a2d6f415c8fb0f1926676fa8c82468b907459f0f66217`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:35:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:35:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:35:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:35:16 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:35:16 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:35:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:35:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:35:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:35:31 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:35:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afb1940e1bdde2fa1c0cfafc70f2e1d77a92d0aab7141eeb66a33a917760c3d`  
		Last Modified: Thu, 14 May 2026 23:35:53 GMT  
		Size: 145.9 MB (145905444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f49c080afc52017a7c00ed91a98ac519cc9b722292a69f9214e30dd73ea8d2b`  
		Last Modified: Thu, 14 May 2026 23:35:52 GMT  
		Size: 72.0 MB (72046633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330b4a1fd6941aa167be5f72c71e58c0ec9ea8e381cda214d7309cf8b517312d`  
		Last Modified: Thu, 14 May 2026 23:35:49 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75930f538daed4ca0481ff92a5ad5371d1e28147d2992d9525813a0e46913530`  
		Last Modified: Thu, 14 May 2026 23:35:49 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:26c98e5db2e58eb10a21f1ced3a2fa73abfaacc9d0ac74ffe467e29315c4ab33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57df2fdf8e35cc2c6860ceddb2766318625155e39d4e093ecff9c96d19ee1d02`

```dockerfile
```

-	Layers:
	-	`sha256:fd17548bd6bddf915dbe3983e762520e35470086e2b0b302030e089fbb9f8362`  
		Last Modified: Thu, 14 May 2026 23:35:49 GMT  
		Size: 5.3 MB (5259853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2b9b35194635282c2f930b95511c50f4a77fcbdab60ebe4c0f54befc51ccf5e`  
		Last Modified: Thu, 14 May 2026 23:35:49 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f9546f5225de990718b771887ff99564160d69401021c0ae753fd0c139ba2d9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246723617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7358c3990a0836251a009c1a12163a6e5d080c729912260481837927b99a7c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:35:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:35:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:35:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:35:15 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:35:15 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:35:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:35:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:35:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:35:32 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:35:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1bfa967161eef18f9c9292bbe7f1ba8a15853c4ab6801a39ba54c59b0bd500`  
		Last Modified: Thu, 14 May 2026 23:35:54 GMT  
		Size: 144.7 MB (144724357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d575b21455a6cf5d70f1b3687fb3c64ee64f1ae8e68e5d324d1f4d9e93379e9`  
		Last Modified: Thu, 14 May 2026 23:35:53 GMT  
		Size: 71.9 MB (71854572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37984c59389f86051bd5d0cc82bdf5688523f5c934f4fec08d57bc773891329`  
		Last Modified: Thu, 14 May 2026 23:35:50 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fc2e62b6d696bb3679a825c1582f2ea21ee47c353e280b7e6f5973fe8954b6`  
		Last Modified: Thu, 14 May 2026 23:35:50 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:58bbb92a7ecff765336c385259d1c3bfa54665c05f7b7159a89ff334036c391f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ca43ea511513ec511b811c670c9f944c5cb5c0511ecfaf5510820df8b6cfda`

```dockerfile
```

-	Layers:
	-	`sha256:cffb824eb73040e9ecb843b3df4f668579be6e87dc9bc98ebdefda58be15e9cf`  
		Last Modified: Thu, 14 May 2026 23:35:50 GMT  
		Size: 5.3 MB (5265622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ddae21b9c3d5cec6e7456e898d077faad6a2f700b5734c8bacb0856849b7939`  
		Last Modified: Thu, 14 May 2026 23:35:49 GMT  
		Size: 16.1 KB (16084 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:24c2fc90087f1edf285845258d6e48af66c114c89e989d371932f5600194a699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256822824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e786d6445403ecfae23fb7789b99e60a8712a43009b410dea9cbe81506f1ff7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:32:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:32:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:32:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:32:03 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Sat, 09 May 2026 02:32:03 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:46:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:46:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:46:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:46:30 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:46:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f72cabc9601635085bc11fa48d74114d9e1765a07685bad636cd3a7da9370ac`  
		Last Modified: Sat, 09 May 2026 02:33:09 GMT  
		Size: 145.8 MB (145766215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0811cffd684aacfd5b7e43c6c2a6bef8f374ce01127847d57cdb1b7f7315e890`  
		Last Modified: Thu, 14 May 2026 23:47:06 GMT  
		Size: 77.5 MB (77457476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20ef5944be4a6bcc8befec199ce406b36887be7626da4069dda99eb5f6fe90e`  
		Last Modified: Thu, 14 May 2026 23:47:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816708c48823aa6a98218f8cdc705c8b2face74e76e97734636d5cff0a0d2d2f`  
		Last Modified: Thu, 14 May 2026 23:47:04 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5f25b2279c8673f310957201c732040fa72e2f1190445b5a1e56f964ac1ec238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6337be21fbdfd0bad77a717410020932185baeca73162ebe7223459fa6c9b8ac`

```dockerfile
```

-	Layers:
	-	`sha256:c777119c83d93a305637c69ee27c30a3dc2e81bfea82a55ebe2c954b33912220`  
		Last Modified: Thu, 14 May 2026 23:47:04 GMT  
		Size: 5.3 MB (5264224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a210c7495d4ff90eb264f6fa930ac5dece57cacfb235bd9f59e8d778e2a9083`  
		Last Modified: Thu, 14 May 2026 23:47:03 GMT  
		Size: 15.1 KB (15059 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:cd2ded439a97ae2f6712c273f1bb2d675fbf4b7c11fdc484690d6b6487183fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.8 MB (238766436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00a550b29cd75946fa91ec8922df6b860676966cd0892fe4e49f64d4fbcf6ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:35:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:35:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:35:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:35:32 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:35:32 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:35:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:35:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:35:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:35:47 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:35:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeabeb56e1eebe9b1edc136c9b084b501f34255e33a2b2c7f5f66dcb37c977db`  
		Last Modified: Thu, 14 May 2026 23:36:20 GMT  
		Size: 135.9 MB (135910407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9c911d36307c87daa4dd89e2501410eb4613332ff7aac33484cd61004419cc`  
		Last Modified: Thu, 14 May 2026 23:36:14 GMT  
		Size: 73.0 MB (73014641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6496676da88233ea4fb8eb4ed7a64bbc437b165e392c4b0ddbe3aebc816078`  
		Last Modified: Thu, 14 May 2026 23:36:12 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fa564538089b6775cf7460a8d48c8c041a651b3e64fcc54bf53029f2e56446`  
		Last Modified: Thu, 14 May 2026 23:36:13 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bb95caedb371846413861572d3081ba51b604e4246ac0a01dc23559ca15d4196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af678208e43fe44189a6dfa80f749b68f16a99ec78c5e9d0a7ab41e0418fd2c`

```dockerfile
```

-	Layers:
	-	`sha256:71f730961d681e914cde60829c65298d48c4d12c3c76f1fc65e7ca241365f24e`  
		Last Modified: Thu, 14 May 2026 23:36:13 GMT  
		Size: 5.3 MB (5255777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21dc0be5ffb154d54d0f73cdbf639e5ee13bc527639c6dcd3bfc680697fe00a4`  
		Last Modified: Thu, 14 May 2026 23:36:12 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json
