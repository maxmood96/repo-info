## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:cad5b4ff4f965e45ed08ba3c67287087fa1214187f5d5dc4f5bba258401e4409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:452fe13da55efa7e2bfaaede37954cb5b324a2425be1d41276d47e249527f76c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269373641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f217c5d46fa5c9dd7776122c051e0db08ca9ff7dcb42c0af17956d6888bbe959`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:11 GMT
ADD file:ff6bc341b5945acf6b9c190d70b5f5806fb3fae7b5c568ad6395aec1b95ba89c in / 
# Tue, 12 Mar 2024 01:21:11 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:12:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:59:10 GMT
COPY dir:4cef005a87cd4606dd69ccb04c755a46f4aa2c925fb1aacc59928d64687208f2 in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:59:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 03:04:43 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 28 Mar 2024 03:04:43 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 03:05:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 28 Mar 2024 03:05:03 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 28 Mar 2024 03:05:03 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ec335f17d0c74f7a270925cb1bbd29acc72ae904c6f4570f9ae369e3eebb64ed`  
		Last Modified: Tue, 12 Mar 2024 01:25:59 GMT  
		Size: 55.1 MB (55084969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda920a039665a5015c5cb162e10882e5997cc683456c339212c7aa546a6ebd7`  
		Last Modified: Thu, 28 Mar 2024 03:19:51 GMT  
		Size: 145.3 MB (145271223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16d388334fda72b4c2c597edeb18cb82f1ae5649af08ee7f4a7abfad702b0e3`  
		Last Modified: Thu, 28 Mar 2024 03:23:00 GMT  
		Size: 69.0 MB (69016830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba12952468949a219a1c9ce2486eb1367531b9db802d4ca35bf391c586dac513`  
		Last Modified: Thu, 28 Mar 2024 03:22:52 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:91265d2b3bd779a35ad92584756230d9f269af10d2ca2d34d572b95535183cd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.9 MB (264870795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff5cb2e9311943ce023ce74eedd3c14d10aaa6e19f88fb51203e3923ff8a3b9d`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:43 GMT
ADD file:7cb312b5f676a37f5c3172be6eb95e30986e5da0dcf21985d2176f8a9a037012 in / 
# Tue, 12 Mar 2024 00:45:44 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:44:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:33:19 GMT
COPY dir:d5fb8d9a38dea7496f2aff176bc9a34bbca80551c2dc57109d2dae5907a339ee in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:33:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 02:37:48 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 28 Mar 2024 02:37:48 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:38:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 28 Mar 2024 02:38:06 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 28 Mar 2024 02:38:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f53ee134f2f58aa9d86f682cbedb185619a5b857474f430e6dc3384fafdec81c`  
		Last Modified: Tue, 12 Mar 2024 00:49:12 GMT  
		Size: 53.7 MB (53722099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1fdda8e4da6bde8ae6730609d8d2464cbd336e3514cb984622194caa155ea73`  
		Last Modified: Thu, 28 Mar 2024 02:50:00 GMT  
		Size: 142.0 MB (142006317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f154bb144a34aa269490b9eb3ac10ae0b5df1ca8d3bf80066a03377ad4111a2`  
		Last Modified: Thu, 28 Mar 2024 02:52:32 GMT  
		Size: 69.1 MB (69141759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:494b8bbdf0ab69914069ef001a5c687dfe925395dceb5f87a84ad42ef4b033e1`  
		Last Modified: Thu, 28 Mar 2024 02:52:26 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
