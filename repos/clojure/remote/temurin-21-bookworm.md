## `clojure:temurin-21-bookworm`

```console
$ docker pull clojure@sha256:c141b3d2338206e7ad8958c8553ba8275d2b3ef8a3e6fe1fbfabba731bad0b27
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

### `clojure:temurin-21-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:b5f2697044d8de70441699d8e4c76aefcb9c0d936ba30c967a96d8a7ebadf4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287122969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2ba90a4ca377a878c051aa0b981caa07f91145776ffa45bf132c144b687af3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83775a042eea68bab319387a3850ef5d25544f864bc0664fa3b84d1c996e522`  
		Last Modified: Wed, 02 Jul 2025 06:55:01 GMT  
		Size: 157.6 MB (157634471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4ea4c3f988e1cecc927edb0d136c9143bf2d99241507b8bc06952c2881ba76`  
		Last Modified: Wed, 02 Jul 2025 04:17:31 GMT  
		Size: 81.0 MB (80993174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d0823b0e04a15c8ec415c22a754f6b2f187d15c8d392109803e70789e2d49b`  
		Last Modified: Wed, 02 Jul 2025 04:17:21 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6c5ef3e9ed08ac8c7fc7f04e86b18e4c6cab2cbbeb52c06487c084d6ef31f3`  
		Last Modified: Wed, 02 Jul 2025 04:17:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:89e0c486e5cfdd45ba6a1fca3e3ccd204ed65e8540820604dab2202b19ad1a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7391191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82cfe92382b2da0d837f769ca395df4ffd16c8b97ba1ea2ff853af28c8a10905`

```dockerfile
```

-	Layers:
	-	`sha256:cb2098c5fbeecc8ac24acd6c429a7f5ea2350a87c7f233784d35877b95e08789`  
		Last Modified: Wed, 02 Jul 2025 06:39:15 GMT  
		Size: 7.4 MB (7373370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84c0482506dab8508bc29b8c67d78359a566ca49186359fae4304cd1f4b578bb`  
		Last Modified: Wed, 02 Jul 2025 06:39:16 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a9dcf1cfbfc0eebba73cd559b5f18965f503b53cb2ccd90a8603fbb6eeea4019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285120448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13591c511bdaeace269183b036203ce2d737244aed6a40c5e66e82ebdb814411`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b9de8beda4a757137961b46cecf6ef375e78c6d0d30df0480ccb9a9a663231`  
		Last Modified: Wed, 02 Jul 2025 14:13:14 GMT  
		Size: 155.9 MB (155928803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0957923c19312b121366ddf6263908e0506ee8200e07e27c323f6693ee355d9`  
		Last Modified: Wed, 02 Jul 2025 12:48:55 GMT  
		Size: 80.9 MB (80851819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680ca937b82a95ec180b1ba34e4de3f968628dbe5e03e5e3ba81ec6a59c11cc1`  
		Last Modified: Wed, 02 Jul 2025 12:48:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3fd9bbbb411d815cc4f8f07dd868b1ebb8b066e92c2c1aa7d728830667d0f8`  
		Last Modified: Wed, 02 Jul 2025 12:48:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0b20000fce8ba5458c4a62acde93cd9596da70e51d86bd13d58d7bc1fe301257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90fe9f6627f8b0ecc6ae012d19ec035a89731b3f66b42d9eeed631d3588ef447`

```dockerfile
```

-	Layers:
	-	`sha256:041b0422042f7e392d46c1d367208581fc4d738a036de135cd182697dfc0e9d6`  
		Last Modified: Wed, 02 Jul 2025 15:39:32 GMT  
		Size: 7.4 MB (7379205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3b448588b4dc69c564c69f560e46fe88a33c542586263702c054a8da8f14a53`  
		Last Modified: Wed, 02 Jul 2025 15:39:33 GMT  
		Size: 18.0 KB (18009 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:d4d5292fc3ea8da44c56fb1d5702a542c755d53821a7db9d67e7e7d6d4e1001d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 MB (296963152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff59ee2513a4288666e219329d13c49ddd59af4886896f4eab965d083d98bdf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b70a20394afe1554f6dcfab4336f53499f8ebb7f9157cc68096ca586b6c720`  
		Last Modified: Fri, 04 Jul 2025 19:13:18 GMT  
		Size: 157.8 MB (157804888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaa282a9c5844e33ee0dbaca1e79440cfd6d7e17da0840840045436cf7e5a92`  
		Last Modified: Wed, 02 Jul 2025 13:52:06 GMT  
		Size: 86.8 MB (86819980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57e223b1ba8be4caafa9ff0f1b22a111534e583098710cfc185a5376d719144`  
		Last Modified: Wed, 02 Jul 2025 13:51:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362bf6e755e1204944b282b72fb3f43a9c0454d8f9ca5aaab6e1cd428aadec2c`  
		Last Modified: Wed, 02 Jul 2025 13:51:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:60f08183d3564a500f9a7f73d76a103062386b302cd40da734f377d2b61d37b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7396515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fab885396a2ed36bf9290258f5f1dff7eda5ba2ee0e92c98c9277a0eb52d40c`

```dockerfile
```

-	Layers:
	-	`sha256:0fb8fc324848312e0240cd95beb535474aabed8957917dac2182e12e59fc95c2`  
		Last Modified: Wed, 02 Jul 2025 15:39:40 GMT  
		Size: 7.4 MB (7378610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40393449d927d7b4e6e9ee8fd638a2a1e7b137d5fbb19829b6f839075fc01865`  
		Last Modified: Wed, 02 Jul 2025 15:39:40 GMT  
		Size: 17.9 KB (17905 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:f215f39c0e9fff0e829e044bd7af8dc5b3f8351c3be5be60f7449d3a617414ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.9 MB (273861028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff6ddd3462f07aae7859e3888f1d52bf18b37506d907cb42072d868ae2413a3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71823214ca06149a34c4a5c5636a79e89289c740013a636fa935b1f75f3bcb3`  
		Last Modified: Fri, 04 Jul 2025 19:12:17 GMT  
		Size: 146.9 MB (146910978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5eb5092fb5373777904bd7a977d1809081a8c2a23bffc471983c1c296016ff1`  
		Last Modified: Wed, 02 Jul 2025 06:50:36 GMT  
		Size: 79.8 MB (79799721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2b2b10a4b8fad61227bf28196539fe0fc1e30f2d55925994e69364034ce98b`  
		Last Modified: Wed, 02 Jul 2025 06:50:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e105eb8a3d6703497bd5652a0f6b0c8df720ac6c849b87cf136f05289da705`  
		Last Modified: Wed, 02 Jul 2025 06:50:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6a0ebab53d9bcf3563018a03034679fb224f50a66d66041f355cf555fb4bb25d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7382510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233fbacac97e0c7d590a1f484e154c85ac272085a045aed27c1d6877908bbf1a`

```dockerfile
```

-	Layers:
	-	`sha256:054cdf872d5d2b5844c3e4bd8a44f61c7608253efc4a6540645a44cf2a68aba0`  
		Last Modified: Wed, 02 Jul 2025 09:38:56 GMT  
		Size: 7.4 MB (7364689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c5a9e39573b0d2d0e32d1ac0a3ae664e948fc3297a6686f3fbedc313f28b4bd`  
		Last Modified: Wed, 02 Jul 2025 09:38:57 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json
