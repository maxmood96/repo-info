## `nats:linux`

```console
$ docker pull nats@sha256:820ad2d9df258d84c84b9f2221d7c26ade4cb6d373414fa0a281ec0242e74454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:b019ab4dc5a25b2a5d5bcdca293d7d1a9e3be245a8b2c19ad141b44141e7e8dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84fba56e41e21dbfcddf8da36ae26dc658afd1e75c261618e4222428aeda1d0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:1fa7823acfd2250002eb8f50b8141328330d40e8bbb0ec239c9f4a68fc82234a in /nats-server 
# Fri, 12 Apr 2024 01:05:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:05:01 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:05:01 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:05:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ef976e251d385162e278fb7189326028787a285844b72a5f08ad011e5bcd812`  
		Last Modified: Fri, 12 Apr 2024 01:05:55 GMT  
		Size: 5.6 MB (5555181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964eb73c0df79bea647bbf87d98cb4254890536cf6182c874f5ddf7a40e77deb`  
		Last Modified: Fri, 12 Apr 2024 01:05:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:ce8e0aea3a34558329944bdec99a8e496dbe2a6562b65c600a2edfc942c0f287
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1595102e5d038c931fe296c06feb2615d823c5d87cd44fa5314566f3880be29f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 00:22:57 GMT
COPY file:e76d33e61cd3b9e577dacd4e007bd874af848278e0854061be93a573166b019e in /nats-server 
# Fri, 12 Apr 2024 00:22:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 00:22:58 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 00:22:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 00:22:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eab7111d77256b9bce6b11f21f4b3a500f34c47cc4c8d1fb178eb77115b60baa`  
		Last Modified: Fri, 12 Apr 2024 00:23:48 GMT  
		Size: 5.3 MB (5269614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db73e1394004bf33be9ddcae480a6fcfac6607af999adcd7e66eecae86993b66`  
		Last Modified: Fri, 12 Apr 2024 00:23:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:1bc22355dbbd74f9b001944d5d16131dad5cdc0fd9d8135d6f38d6ae1871ca5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a436981dde34308e225bebc3181dc0e261f9b374c3878cc79e25ed148c2092`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 02:09:37 GMT
COPY file:fa0de21665d2f20e57f0c4a2ad42a2a3e8d0eba2e678097f1755d8ece05020f1 in /nats-server 
# Fri, 12 Apr 2024 02:09:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 02:09:37 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 02:09:37 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 02:09:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3d33c9b505b063b46bca30c698e05482b73046ffa3cf3fac3469f96dc2792514`  
		Last Modified: Fri, 12 Apr 2024 02:10:28 GMT  
		Size: 5.3 MB (5258628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddb060b0da3f0952a7e57a738ac4c7d96d3fe1e7247a76eac3c19ca34a48652`  
		Last Modified: Fri, 12 Apr 2024 02:10:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d81373cc12a6d4755503e7f0f7237ee0e4c5083419441978cef475682dfb6520
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e7b636900ccce42ba6585cf9a4940be53a4b9719a046b220d669a4173ef5df`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 12 Apr 2024 01:17:09 GMT
COPY file:30639b3b4cd3f0ae1787ceeaa2d87150d04ee61962cad716be1c72f5ccd59993 in /nats-server 
# Fri, 12 Apr 2024 01:17:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 12 Apr 2024 01:17:09 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:17:09 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 12 Apr 2024 01:17:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:296ddabfcc8c0c5534dff91df9174a17c9d95d6cbd623b14f6847b16e8672a15`  
		Last Modified: Fri, 12 Apr 2024 01:17:59 GMT  
		Size: 5.1 MB (5122105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a262f77d0832725628d122e67128d2d4714582f9f2c7f3471b2788bf3607e7f7`  
		Last Modified: Fri, 12 Apr 2024 01:17:58 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:fa1b571a231c51f186cceb7ceb74aa11629fc13e246c893c9d2b5961c2d6f33a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb680a4e05ff0c3df664d1f3273e8bd4d73826b66900295ac89f920567c24f66`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Apr 2024 23:28:48 GMT
COPY file:eeeb4b354c6d56eeb52c70ca1d80bd57f20f72542a60bb6bd8cdf02459eaeef0 in /nats-server 
# Thu, 11 Apr 2024 23:28:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Apr 2024 23:28:48 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Apr 2024 23:28:49 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Apr 2024 23:28:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b2bd487f26020167d95341f4cb66eb039be80b49bb43a84a0aba2aea55a89bcc`  
		Last Modified: Thu, 11 Apr 2024 23:29:31 GMT  
		Size: 5.1 MB (5099968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d35b10dfa7b5a98e052c538c68277846d816f7efcb93521e015e33022a5294`  
		Last Modified: Thu, 11 Apr 2024 23:29:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:b200d259ef6d710b801ba60a7f296791ebc5298d82db48b8f68cfc0bee79d15b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26134424de3ad1af4ffe096901272e7ea3dae1a93eeddcd6c110b08b29af4011`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 16:58:41 GMT
COPY file:cc94c349de0e266f428d63773845fb669334304c5fbcffeec57553d333126f22 in /nats-server 
# Sat, 16 Mar 2024 16:58:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 16:58:43 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 16:58:44 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 16:58:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0bf838b872f1e012c580bbff8d1e66a09a7b05a85651db222851ea3323dab3d2`  
		Last Modified: Wed, 13 Mar 2024 01:16:47 GMT  
		Size: 5.4 MB (5430321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea5f20b9222048fdae4e26dc03a3a997375533021a900c72f4e6b338c144ddb`  
		Last Modified: Sat, 16 Mar 2024 17:00:32 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
