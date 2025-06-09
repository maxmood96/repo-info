## `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm`

```console
$ docker pull clojure@sha256:0707a741a10aa7fb3a624f9c8e459969843458b6b6dafe3e29c4fdc4fdedda2d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm` - linux; amd64

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

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

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

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

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
