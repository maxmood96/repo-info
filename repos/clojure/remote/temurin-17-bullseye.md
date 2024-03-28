## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:9f415e8333426bbdddbb7f647c476a4b9eb65ac6aef03e4bc67d28b0bd80b972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:546ab8335df2a4ea0cbb953f2ec384b68c38c3f58d1a3c9d8d0396f525bca76c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268995380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2793307e93da2fb80c33f579b2a08b0e4066cf9831c8468273fdee265cf04f8b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:11 GMT
ADD file:ff6bc341b5945acf6b9c190d70b5f5806fb3fae7b5c568ad6395aec1b95ba89c in / 
# Tue, 12 Mar 2024 01:21:11 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:12:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 03:07:20 GMT
COPY dir:88c5118aff6896f6ed535dcde576d68ef88ded459cca013e0f9beb3e430ebb52 in /opt/java/openjdk 
# Thu, 28 Mar 2024 03:07:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 03:12:36 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 28 Mar 2024 03:12:37 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 03:12:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 28 Mar 2024 03:12:54 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 28 Mar 2024 03:12:54 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 28 Mar 2024 03:12:54 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 28 Mar 2024 03:12:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ec335f17d0c74f7a270925cb1bbd29acc72ae904c6f4570f9ae369e3eebb64ed`  
		Last Modified: Tue, 12 Mar 2024 01:25:59 GMT  
		Size: 55.1 MB (55084969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40bcd404f330742d08e449c864937a0247411adf1e0630d702b0d270a8c84eae`  
		Last Modified: Thu, 28 Mar 2024 03:24:58 GMT  
		Size: 144.9 MB (144893082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c9b70b583235b97d2b295e4ae2e955dfc1d99a91900c0f58181aadb8c46d01`  
		Last Modified: Thu, 28 Mar 2024 03:28:01 GMT  
		Size: 69.0 MB (69016310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3bced28957d64c7b3cc32712980f3a914279c13156e0598bf7ad1fb58b4960d`  
		Last Modified: Thu, 28 Mar 2024 03:27:53 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0eb9590678928a1a71dc28a97c2af5092776d6ad29bd57b02454ec060769c9d`  
		Last Modified: Thu, 28 Mar 2024 03:27:54 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f307e3b854d26c55dbf4f594cf29958977801c8edd8a8c4f989fe93f006c5569
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266585854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b07d63e11419e1702e6dad21ed18073e98ef7b9334b1a95e7834ac466507771`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:43 GMT
ADD file:7cb312b5f676a37f5c3172be6eb95e30986e5da0dcf21985d2176f8a9a037012 in / 
# Tue, 12 Mar 2024 00:45:44 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:44:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:39:59 GMT
COPY dir:a5d0039514ccd79689a0ea6094d70ca92113e8cbcc38d473b7c0fcc04a1f496a in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:40:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 02:44:15 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 28 Mar 2024 02:44:15 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:44:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 28 Mar 2024 02:44:30 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 28 Mar 2024 02:44:30 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 28 Mar 2024 02:44:30 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 28 Mar 2024 02:44:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f53ee134f2f58aa9d86f682cbedb185619a5b857474f430e6dc3384fafdec81c`  
		Last Modified: Tue, 12 Mar 2024 00:49:12 GMT  
		Size: 53.7 MB (53722099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fcbeb5850480786ffe08e1502f043ad8bc5d2f3b44ca90dbf17efaa841dacb`  
		Last Modified: Thu, 28 Mar 2024 02:54:18 GMT  
		Size: 143.7 MB (143720923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d83b3c3708874f99e207edcf69c7c30a8bfc4ed42e832380346c1c955b3221`  
		Last Modified: Thu, 28 Mar 2024 02:56:48 GMT  
		Size: 69.1 MB (69141812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcaf179f4e0552eddcdde0cf2861fe54e09287081e4698a87ea3d9f08cf8c9c1`  
		Last Modified: Thu, 28 Mar 2024 02:56:41 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f51da9435b87549abc1114656587d8dd564bfccf3a876d06ba43b7c6742f4ca`  
		Last Modified: Thu, 28 Mar 2024 02:56:42 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
