## `clojure:temurin-24-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:15165968c96e121df89bf1f97dc8eb0071d7369a7c6afafff8aae1a906b802f3
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

### `clojure:temurin-24-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:35d07b89ab88b98c6c46729b602df64f03eaab18bba90fdb8317c16f088555f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219435039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e6854ef33e5ff7f63b075bfd452b16ce521a27be02feba52fe5b093a8705a1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031e646a59aaed67a42989346d63f4749d87821f3ff3333fc7e4f9e44e5ada5a`  
		Last Modified: Mon, 09 Jun 2025 17:19:12 GMT  
		Size: 90.0 MB (89952003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4487db9f4ccde76e7a8ecc6c8db4088a0f8afef217cd54bc4d983af337b6e335`  
		Last Modified: Mon, 09 Jun 2025 17:19:09 GMT  
		Size: 81.0 MB (80993750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829c6803021ae9b289c7699ca2253ac8d5e02c04fa88916d98302f4fa6a09f2a`  
		Last Modified: Mon, 09 Jun 2025 17:18:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5bae33f00deaadcd1deb7dcbaa8b9ece75054ed7c1ce9617fe2248ed67ce0a8`  
		Last Modified: Mon, 09 Jun 2025 17:18:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ad8f8f0f98f2cd1c6d4773aee05d5a174f1e09b60d89a0d9d74f1c76153d77ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7334740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f967be49cb2b3e6fb9e146450b10ba8a32b19a60c34d54a19e0161ab8960d45d`

```dockerfile
```

-	Layers:
	-	`sha256:cbdb2be505063d42b00026823d984fa665651395d247f61549ee93eff557b7be`  
		Last Modified: Mon, 09 Jun 2025 18:40:53 GMT  
		Size: 7.3 MB (7318242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72c6e84406292168a72ced2ae8b2b0f68d76294b4eccad5b25c196a72a7b18c2`  
		Last Modified: Mon, 09 Jun 2025 18:40:54 GMT  
		Size: 16.5 KB (16498 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c7d211c68aba1e8594736028459c4bab0686f79323b9cc6a7eaf9035a03ba953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218267968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee32ffc614cb8f5592224b95699ed76219f153937d9c44f0e4975f71bca88357`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad72b0b0d87ada56df9b871909e981f1cfce883a2eef16b29952fa54093bf67`  
		Last Modified: Fri, 06 Jun 2025 12:22:32 GMT  
		Size: 89.1 MB (89091274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a62bced74f1b20a5127e762350827b310be1b7c43e0658eb60c0ae665cada7a`  
		Last Modified: Mon, 09 Jun 2025 17:58:43 GMT  
		Size: 80.8 MB (80848473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c031238fdb252be7d1ea5600866d801893d81a569006716fc62c6c8ae76313c8`  
		Last Modified: Mon, 09 Jun 2025 17:58:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db56df586f0ac678aa2fa2e7bc38c632ba7913482bd7dfc229a68d369996cbd0`  
		Last Modified: Mon, 09 Jun 2025 17:58:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:485db1c97f0ba4a60b64be61d4a9844b5799bf6652791ad7570563ad1eda4af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7340666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d91118e3a64ed376d63afcf3e819b369ca5570be80b3aca63d49a65d3d32d66`

```dockerfile
```

-	Layers:
	-	`sha256:c1a29375b4418ecbdfd9d5e90da640114155d23b558545dd8de382918f2e6a3e`  
		Last Modified: Mon, 09 Jun 2025 18:41:00 GMT  
		Size: 7.3 MB (7324026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01c7b64c01fe70de1fdd66a1ecdd527f96588df24b6fe8b734dc68ac746c2077`  
		Last Modified: Mon, 09 Jun 2025 18:41:00 GMT  
		Size: 16.6 KB (16640 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:2fe9ff6de28034780d80baa48bbbbfdafd7372971a244028462a8b003bc9bc9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229066363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3baf9d88199d292eae85c50d298d390de48354e955758d13025669166202e144`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3937d64ddc56eababfde7af2e4d4da5a1866df46d7de0bebf9c2a99e0b0cce`  
		Last Modified: Tue, 10 Jun 2025 11:53:34 GMT  
		Size: 89.9 MB (89920270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba905a300ca853c2ae9af60210c1f6a832d35f4bfc7cca5369326613e75cc8b`  
		Last Modified: Mon, 09 Jun 2025 18:22:23 GMT  
		Size: 86.8 MB (86813429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babd5faa9df6fb4ac51905ff2a5ae9aea82c359321020fc43a4ad3b92d795d30`  
		Last Modified: Mon, 09 Jun 2025 18:22:15 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892c33fcb5f30c34c401458ccc728bc219f6c14011fd1d9465a058b8c8467fff`  
		Last Modified: Mon, 09 Jun 2025 18:22:16 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:789cd357ea46c43a1bdbed0f1a8bfec1a79da556510f598c78ab5297f99da94a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7341313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b355b1ec4da3b72323ccc15a1087ea708fc163793d09759b6268ced6785ec7`

```dockerfile
```

-	Layers:
	-	`sha256:8112acc032e6b247f081357f3e155b1a178d17e017817d9e10484b1e1433ec90`  
		Last Modified: Mon, 09 Jun 2025 21:39:04 GMT  
		Size: 7.3 MB (7324756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e5453d4d00ed118454c853e75e172a78ecbadfbee1fbcbe9a9e31f98e600272`  
		Last Modified: Mon, 09 Jun 2025 21:39:05 GMT  
		Size: 16.6 KB (16557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:8cb1d3b29f3c763aa57d3bee8e695489f896a85e65420afcf07cb15f6d4279bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212164315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c860e18c55a0998c588057951406693dc5a8dae61eb063b6b583b9a0ef315fae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Tue, 03 Jun 2025 13:33:39 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a88af61dafe611dbf396e5a57107bc7b7f88c5b3a0ba26ce314843717b096f`  
		Last Modified: Wed, 04 Jun 2025 04:17:26 GMT  
		Size: 85.2 MB (85216876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89fae121f8fa76eb1865f7afd835256c46eb341246b53d70881706a9fce8bca`  
		Last Modified: Mon, 09 Jun 2025 18:58:12 GMT  
		Size: 79.8 MB (79802559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855e6d9506356ca122beb5363ca13cfe56cbf915bf9d0ef9c48d8b6c7bbd8bd4`  
		Last Modified: Mon, 09 Jun 2025 18:58:01 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4dddfeb00634535ee074f58ea93c401bacc5a656ecf536d5cd2f16e12448e8`  
		Last Modified: Mon, 09 Jun 2025 18:58:01 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:dae0b316d04f6b276b1054cbc8c8bdf6a1e9b594a8f787ee764d9e52695e07c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7328606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd08fddafc51b11bc429164ec53ea1af475be18c7b9f8b6854ee07dcb4945392`

```dockerfile
```

-	Layers:
	-	`sha256:2eec4f187256b1bfe0fd8253f2801b526bd153cd4aa726731609aa1f4b942b1b`  
		Last Modified: Mon, 09 Jun 2025 21:39:12 GMT  
		Size: 7.3 MB (7312109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2e06657bbbf18bf41bbb797af690dd3f5ddfab7eca4d69b13ff76c4d9d7bb62`  
		Last Modified: Mon, 09 Jun 2025 21:39:13 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json
