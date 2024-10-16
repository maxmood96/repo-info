## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:7aeb0e7077e6adc4c6e7807a715b4f3e1719080811ae15a907af1d342ee9f5ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9c2819c9c2382726bdcdd9740f48ffb31e9c119335c3e81ca4a338626cd962d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269582501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4348a2d20813741c8856886fa7c4a2c62893fba7342f866ce8b0dc42e5469a3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea700eacd0370f13770e413ac0c69a03a2ffa5313958e91d81894d8240148094`  
		Last Modified: Wed, 16 Oct 2024 16:13:09 GMT  
		Size: 145.2 MB (145166552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfbdedb0dcd39511e99febfcd1a1e6aedb312a408fcf37e2c80b0121e70e9d1`  
		Last Modified: Wed, 16 Oct 2024 16:13:08 GMT  
		Size: 69.3 MB (69333515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69aa63a636b7becd70fc678c00633c765b0278b40bbd9e85cc40f00e989758c2`  
		Last Modified: Wed, 16 Oct 2024 16:13:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebaae195a0eaf34da7a5ef528502f9d8b8339d39f2a12e75c7c866fe54840016`  
		Last Modified: Wed, 16 Oct 2024 16:13:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:968fedff9ce0b63da7cd34275220077c4c27caff4a945ecd54098f30b5f522cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7204841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c161f34fd0e80738cd317cbbd0bb4c54b41371c6e9bd0637032b0c1df2d12711`

```dockerfile
```

-	Layers:
	-	`sha256:64c140bafd65fb9c5e1b5e57c427ed0a4f4957f6173ea65f09d25de101b83089`  
		Last Modified: Wed, 16 Oct 2024 16:13:06 GMT  
		Size: 7.2 MB (7189363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82eeea44e62d7f0ed55a51cdd6a78ce8905fb02e92fe28280148f6513356ebd0`  
		Last Modified: Wed, 16 Oct 2024 16:13:06 GMT  
		Size: 15.5 KB (15478 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fb903857ec5338ed943dc1210907780ef0c6ee7113dd5c7346cfaab441c7a963
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.2 MB (267161593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f89788ae1d2efc997f2aa5615769bcdfd13c230fe812548887f63d8a80b37b72`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7bffc00dde25142de9c36d297b5f3ec79b326da54b5ebba4f0b05db8be8992`  
		Last Modified: Wed, 16 Oct 2024 02:23:02 GMT  
		Size: 144.0 MB (143959504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d375a3bedac10629f44e68e76c56102179bebca2f778d4f89cd58c8144183280`  
		Last Modified: Wed, 16 Oct 2024 02:29:14 GMT  
		Size: 69.5 MB (69467180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad555b584644bef5118375e85c4c334ff019f667f3b92dfeb7c9dd6d9904a757`  
		Last Modified: Wed, 16 Oct 2024 02:29:12 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ac2c862a0128bc691c03ee4cc01596c2db49385186dfa4b061e46e3bd56e71`  
		Last Modified: Wed, 16 Oct 2024 02:29:12 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:54f77492b0544a97d28f0cabd46ff7ed5999beb7c25009d51c08754529e95cf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7210048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d800660760e620bc81f08483c3ba87ac10328f5db62e814afbcabac2f70a109e`

```dockerfile
```

-	Layers:
	-	`sha256:c85132304d8592db0ff57a60556807e53d4a051d5aeb5a0b3c3696994bf6247a`  
		Last Modified: Wed, 16 Oct 2024 02:29:12 GMT  
		Size: 7.2 MB (7194466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62d6b955f861e3ee447ff0e2484e9014b62edae85b39dd3cde59c5d35386f899`  
		Last Modified: Wed, 16 Oct 2024 02:29:11 GMT  
		Size: 15.6 KB (15582 bytes)  
		MIME: application/vnd.in-toto+json
