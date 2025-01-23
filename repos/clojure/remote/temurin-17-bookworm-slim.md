## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:3c458c7dafec8b61316ead93f273dbb4c82f5a2d40f2cbd54d56c42fe2599996
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:17adb35c51bddf95c22815c330a31b5e71cbad691aa516ea5365c7d7a5cd121a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242276642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2651ca7e1b35eb52f78a55da9bf41780ca142dfd8ca780f9afd384d0417cfc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcc194a49e33efa8efdb8d31de5c856518ac1d238962e21876da429209aa637`  
		Last Modified: Wed, 22 Jan 2025 19:42:27 GMT  
		Size: 144.5 MB (144536778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c930824a6299eab5d8cec745b2cee515e46227cbf53cd234a311a446df10a011`  
		Last Modified: Wed, 22 Jan 2025 19:42:26 GMT  
		Size: 69.5 MB (69526403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60fa97a9579261ff0c92b4b93b97fe53e6839b8b396ae1b442015c3ef651f38d`  
		Last Modified: Wed, 22 Jan 2025 19:42:25 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832ebb8ad997bfc1d91b5edc59cd3a4b4854cd950c6303ad6c5038f6ebcfdeb4`  
		Last Modified: Wed, 22 Jan 2025 19:42:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:302368d2da4adc9bc70c84f5c1b3041f006e82ddab8d59867e2bbeb96eba5289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e94b6d117ba65a10d04c50aceb8fe45ac165e3fcad3dcc19b17bbe5d99466674`

```dockerfile
```

-	Layers:
	-	`sha256:bad57564512a282b23842631e7fb0772506943529f8dc5a4948d31bdfb55ac57`  
		Last Modified: Wed, 22 Jan 2025 19:42:25 GMT  
		Size: 4.9 MB (4912569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fc5beefd54b5f81237aab4db8b7358bba5950ae187ad9edd45fad0caf7e3f71`  
		Last Modified: Wed, 22 Jan 2025 19:42:25 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7c94e258b7940277847fe02f82e3d85aecbb0f555f65cc84ad322612deabbad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240777271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a69dbdfb086ceb095f35b2bd5357311e3f6e1049f48e80fed75678185205a48`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878dbaf01d60d6283547f2fcdacc51188fdfcc4d98d56aaeebf2a89c4dd97862`  
		Last Modified: Thu, 23 Jan 2025 02:45:16 GMT  
		Size: 143.4 MB (143360974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45777180407eef63d9aba1224244df17a3c416d5c6c308c985b9ae2d90ce12e`  
		Last Modified: Thu, 23 Jan 2025 02:50:11 GMT  
		Size: 69.4 MB (69374223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111a05ff5a709523e4939189f685fc197415730d45beb716b8461fffc6bb608d`  
		Last Modified: Thu, 23 Jan 2025 02:50:09 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2f19fd521918601c7b1d5956d6f4184d204280fc14a35759e68bf84187f38e`  
		Last Modified: Thu, 23 Jan 2025 02:50:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3dbae067d3c2da686e9f3c7314d40becf5e073a93fcd81143aefd6eaabec37bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4934327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f3d76b698576422164b07474a0b7f5631835b9b3e52cfdcd3d9ce8bf76bb71`

```dockerfile
```

-	Layers:
	-	`sha256:a79c0c86c56c2b7d43ca11a635ed00c4d6440cf9066c09f51bbecaa25e63effc`  
		Last Modified: Thu, 23 Jan 2025 02:50:10 GMT  
		Size: 4.9 MB (4918330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bbe4bbbf859bcc72b2756f014d22fbff3ec55ebf70c463f1f74b5cfc06ee4a6`  
		Last Modified: Thu, 23 Jan 2025 02:50:09 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
