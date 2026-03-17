## `clojure:temurin-8-trixie-slim`

```console
$ docker pull clojure@sha256:02cf760a1bfb5fac33a07440185e38b23b9457d2a6f61b32bc1487ad11f2c667
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
$ docker pull clojure@sha256:9482e1b4329112ddf5624bbf6ef5378497c91a8e0a9c0effbadff36523388279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (156958561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881363a5dc445cdc218ee928e48ed951e200e170185285f0d78065f5fef764f3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 02:56:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:56:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:56:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:56:27 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:56:27 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:56:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 02:56:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 02:56:44 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1235e5e524698d8e77c339f1475b0466c7825667d06457e52fadefecb4c16d8b`  
		Last Modified: Tue, 17 Mar 2026 02:57:04 GMT  
		Size: 55.2 MB (55170146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16a53dd92e578715ea16e939f8aa9f1b3094aab34e7a20aa143d4f8250a9aca`  
		Last Modified: Tue, 17 Mar 2026 02:57:04 GMT  
		Size: 72.0 MB (72012270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51506eba55e3d946f88f1f3773697b39110b14ecb625076a1d7b146057cc5bd9`  
		Last Modified: Tue, 17 Mar 2026 02:57:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e73e95e0e44e1affca179ecf7b9edf0bf03b35095af887a29b740f6f23e33d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5394353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2adb71b183ff5bc4469b2183f38290271a1b0ca78c463c499d7a3f08e673353c`

```dockerfile
```

-	Layers:
	-	`sha256:8422866e29abe8917f344e3875190399253056a244e7606c96806d0fdc5173c0`  
		Last Modified: Tue, 17 Mar 2026 02:57:02 GMT  
		Size: 5.4 MB (5380125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:435f3b287dda78714ae7e4dbbd20fdc18c101c5c1952727fa9e9f434a4ea40a4`  
		Last Modified: Tue, 17 Mar 2026 02:57:01 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0f32b3db3c6238ff41058e77b1ecf94ab332cf2e72ac05b1c776106b8d924b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156222007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4d64764e77270b9220671b13eac4cb176fbc85fa3cce0436729b6731531c9d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:00:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:00:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:00:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:00:55 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:00:55 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:01:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:01:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:01:14 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa090f86b86285c3afdaa97ebac9b255cf1410270c664dbf8a700ce0a6ed062`  
		Last Modified: Tue, 17 Mar 2026 03:01:34 GMT  
		Size: 54.3 MB (54251622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09beb11a0a43edbde72a322f79fe4cce79dd63dcc0e75d7e62de9c88799ff5b8`  
		Last Modified: Tue, 17 Mar 2026 03:01:33 GMT  
		Size: 71.8 MB (71831324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08679d944cbb49c995152695eae5f17d6986fafaf66c85b37c9b75bc77475957`  
		Last Modified: Tue, 17 Mar 2026 03:01:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e7a41270272cb1912f6de5dfa0ea67d1c244c6f4b7aaa700a3197663efd6a96e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5400940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7773b519c76bcea695714afdff4f0b6d662cf6390f1f5a8954e2f6827294dd5f`

```dockerfile
```

-	Layers:
	-	`sha256:90f662a5045ebed3c26f3dceb1e805b6c61e38e3f3bde6c8fb3cc398a2e07520`  
		Last Modified: Tue, 17 Mar 2026 03:01:30 GMT  
		Size: 5.4 MB (5386594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb43a6a63de6b86754c4cffe0520338be75870fdeacee0b6d7403c5e5eae455d`  
		Last Modified: Tue, 17 Mar 2026 03:01:30 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:8577c18215f81e3dc33d03201dfca97e64e7ce29bffd3fdc93b93a58d192752b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163673803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42cdde4ee15e8c50f727ba12a4d4fc1fd778eeae0633ccd6b355a6ba69ecdde`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 18:08:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:08:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:08:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:08:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:08:41 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:14:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:14:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:14:44 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf4e66022f0a54019718e5fb82aff975c8ae1279a587e803dd7d8da942e46b2`  
		Last Modified: Tue, 17 Mar 2026 18:10:01 GMT  
		Size: 52.7 MB (52650377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82cc00d65e70e1d3a876d16f2f2407147b4e3661b569bf00c2fbe66a42d9cbf`  
		Last Modified: Tue, 17 Mar 2026 18:15:23 GMT  
		Size: 77.4 MB (77429945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24b651de48ab77e72296b181171877fff8b6264092c79f91ea7268daabb630c`  
		Last Modified: Tue, 17 Mar 2026 18:15:20 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:47b781a99403d516974c6797a08fee829a17eacf8348cf8037f0c0fa0326b2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5399366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b838186e7ccce8cc3da2c020cda1cbb3aabd5ecb15705c6ed469ac42f71a48`

```dockerfile
```

-	Layers:
	-	`sha256:336a822085d8cd5ecb13ac58a2890cf15be97adb75f903c3d9427317ef11f992`  
		Last Modified: Tue, 17 Mar 2026 18:15:20 GMT  
		Size: 5.4 MB (5385091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:904968eef104bc23b0ac15c0a8a670c969d50fc24416932a6c026faa69284c3e`  
		Last Modified: Tue, 17 Mar 2026 18:15:20 GMT  
		Size: 14.3 KB (14275 bytes)  
		MIME: application/vnd.in-toto+json
