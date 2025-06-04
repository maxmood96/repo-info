## `clojure:temurin-24-bookworm`

```console
$ docker pull clojure@sha256:f378e906ea95b887a54ca0252e6f3ac94aee3677c9e9f02c815271167492992a
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

### `clojure:temurin-24-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:91b088c9e1e47c027ccd58228c4fd660e7117fd5c8c10ae99b2ecc1029cbfe4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219435309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c89409bbd17989806241a0aeddfe2c3be2a1c21c9f64be1b6513f690332123d7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fc5e4135ee581b0aa3247eaa73ca7a69af63af36bb774e98902afbadb93313`  
		Last Modified: Tue, 03 Jun 2025 18:24:55 GMT  
		Size: 90.0 MB (89951990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250effc90037a7a686fdab33c66b5601a8b4b505155877f9745ec6a87d95bea1`  
		Last Modified: Tue, 03 Jun 2025 18:24:59 GMT  
		Size: 81.0 MB (80994033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397b5e561d94f0cb61c50d73c0e1b342490ad172a3e61a4b40e57596a0a0df5f`  
		Last Modified: Tue, 03 Jun 2025 18:24:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7023ab0472d7d3b7aa9098ab18dde36da2ccdad24467d23d608906651d1eb590`  
		Last Modified: Tue, 03 Jun 2025 18:24:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5523ac1ec99f45e7a23d4763a1da64190fe3b637a89c0872fc469a8cd3b5bed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7186350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2188d2b85c6b55cbc92541ee14476fbf7963946f55cbfe07ee1c575638acc7f1`

```dockerfile
```

-	Layers:
	-	`sha256:6548b5425aa1082ddc943ac588d05c9909715f3e8dd117da3cfe257cd8c3f8c5`  
		Last Modified: Tue, 03 Jun 2025 21:42:18 GMT  
		Size: 7.2 MB (7169852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35b28311d015207737c1ca172e9a7008510c051e9c5d8a1456970689341b0740`  
		Last Modified: Tue, 03 Jun 2025 21:42:19 GMT  
		Size: 16.5 KB (16498 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6cc50d2b62a509f659c2029dba9e3f50b2b2276742fc1a02fc9847173bdf4659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218268628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eece083e493a1a4771b9393295743d3b08b76a081e0b0ce7b77ed269fccd9b85`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad72b0b0d87ada56df9b871909e981f1cfce883a2eef16b29952fa54093bf67`  
		Last Modified: Tue, 03 Jun 2025 11:04:46 GMT  
		Size: 89.1 MB (89091274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283ccbcd7f8a5954bfbd67ba23390369afbf881ea36e0cb34213a4f67536afa2`  
		Last Modified: Tue, 03 Jun 2025 18:52:27 GMT  
		Size: 80.8 MB (80849133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0411ce299d10d9567699f19722a3d87a5a15ea9d56477c60341718ed758ea6`  
		Last Modified: Tue, 03 Jun 2025 18:52:16 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8f9805fe6ae492ba239463ea8e1dc72d313cd73803238ce63a39b866b194f5`  
		Last Modified: Tue, 03 Jun 2025 18:52:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c0d8fcf52a815e14a9b9080811208c706804345cb6cf9c61ec50439d0aeeddab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7192276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a18492498e4289d29725c84992ce2cc46c8e433990081b9b4c26df610214ffa`

```dockerfile
```

-	Layers:
	-	`sha256:bbfc2a9a983ce9f7c773e9762b51d6f289d8eecbc2e9de50f923523bd76e0dc4`  
		Last Modified: Tue, 03 Jun 2025 21:42:25 GMT  
		Size: 7.2 MB (7175636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af7390d5dddd49fe62e84209d31a8316ba13e07c5e6349ee62eff4a54f911c50`  
		Last Modified: Tue, 03 Jun 2025 21:42:26 GMT  
		Size: 16.6 KB (16640 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:decba4b636c3ed693cd5516cff9b69397d3aee364322609b85808710d1b38bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229066215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a8cd21734c233c479828f66ae12de7f2060e88fb350afa9d693a937ec02285`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3937d64ddc56eababfde7af2e4d4da5a1866df46d7de0bebf9c2a99e0b0cce`  
		Last Modified: Tue, 03 Jun 2025 09:24:56 GMT  
		Size: 89.9 MB (89920270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580c60d050dafc3fe90938635002c916569f416158c3e8dec6b012a64ed67f29`  
		Last Modified: Tue, 03 Jun 2025 19:10:57 GMT  
		Size: 86.8 MB (86813286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d6e9cab8e0acef53e71817f96203fadf283323473ea8bcfdc5c61beb159bec`  
		Last Modified: Tue, 03 Jun 2025 19:10:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97bd8b4cbfadf2bef065083067d87f1cd2d165d67f4427f64541cd6efa3b9fb8`  
		Last Modified: Tue, 03 Jun 2025 19:10:48 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:bcee6c73c50a3f945f8eb5cebb25f041ae2a71cf39aa353c1918d5081612c915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7192924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2c0ce9628d093b15f607898abcff3a2defee26fdd2a10ff111e7b84bfb4800`

```dockerfile
```

-	Layers:
	-	`sha256:7ef8841c1c149e24d43f3e347dc5ef842dea3800476b541d5fb063a3f9326d3a`  
		Last Modified: Tue, 03 Jun 2025 21:42:32 GMT  
		Size: 7.2 MB (7176366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a38daee7f62aa11103284c0007cf3f5d8681bb9bb576d2e180660a8c32429c25`  
		Last Modified: Tue, 03 Jun 2025 21:42:33 GMT  
		Size: 16.6 KB (16558 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:f6b6234a2e3b8581ef842fd8f750141bfa9acf916b4755d975036d0d8b6ff6bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212164646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1604f2e403f62f4d444c07508745e6536455e0056bb296a3e7c95ea57cd17506`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
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
	-	`sha256:6f56832f865b11a2803969cadc6350d8b20eeb1b3b44b974be097308cf5f3ba7`  
		Last Modified: Tue, 03 Jun 2025 18:43:27 GMT  
		Size: 79.8 MB (79802888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82cc649938dd39ae41b23a54911f89f6e449bcc0a9589b30ab382886e873ae62`  
		Last Modified: Wed, 04 Jun 2025 04:17:50 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158ca266184a66e3c4e329b1a4382513108f454baefb7126a1ca2c875bf0bb6f`  
		Last Modified: Wed, 04 Jun 2025 04:17:54 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:82adb49b8f457cad9fa0f8f35c0a09ef9380f28a839ac294ba25f48bbaad3ea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7183109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d33d4120bc9f100774e3356cabd5428742d27ce3adeabb5218dee13b6cb56896`

```dockerfile
```

-	Layers:
	-	`sha256:c99ef41c1ac7e0a5e7d61edb0866bf10797eefef6eaf8ec6093190077429e134`  
		Last Modified: Tue, 03 Jun 2025 21:42:39 GMT  
		Size: 7.2 MB (7166611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bc77dea9169a5c5873c03ab03e7268d53add085c83fe3bb36eb4e4d50c86064`  
		Last Modified: Tue, 03 Jun 2025 21:42:40 GMT  
		Size: 16.5 KB (16498 bytes)  
		MIME: application/vnd.in-toto+json
