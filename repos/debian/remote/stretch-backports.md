## `debian:stretch-backports`

```console
$ docker pull debian@sha256:28be40344c3bbb58f11e57f9c15378abd3dbf2e2c1588bf3fd677cd35124ec77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:stretch-backports` - linux; amd64

```console
$ docker pull debian@sha256:b327bd48bbd65095481056d57709dd61cfcb04a4477d170f9d68faa8680320c3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45380217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72937eed37e1d02280f37a2b0228291fd5dd37f01a5ce97967f4767a11763c2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 23 Jun 2021 00:21:59 GMT
ADD file:899a3c031d50263e5fce253aef92e05aec77f14ec3c38a37f08414e4c9b358f2 in / 
# Wed, 23 Jun 2021 00:22:00 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 00:22:05 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:199ebcd83264652823564822c7ef553db971042e35d7f347f66ea8a60a480545`  
		Last Modified: Wed, 23 Jun 2021 00:28:01 GMT  
		Size: 45.4 MB (45379993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5015609a37b3905c619f653e398e32c25b562d617102a42dd550709d938b19a`  
		Last Modified: Wed, 23 Jun 2021 00:28:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:8173ab3a842a1098f9aaaf0b294b8c5e8ff48c70af47f90516dea0d0482a5b01
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44092275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2679298d48f5f2fb60602b6c15dc2094d9aa3e29c1d321004e712ac1be025c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 22 Jun 2021 23:52:47 GMT
ADD file:ac76479423dbb474270e853128fccece010f64fd8b2cb114c2a35b3da5b74756 in / 
# Tue, 22 Jun 2021 23:52:49 GMT
CMD ["bash"]
# Tue, 22 Jun 2021 23:53:04 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a89c1f87f7fbe989370a717a85446a7926b68d3e20e9344a5078c8c4bb39cfff`  
		Last Modified: Wed, 23 Jun 2021 00:06:22 GMT  
		Size: 44.1 MB (44092051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5c75fe431077e34344121a06305c8c5b335804066588187ff3c92ff8c3c34a`  
		Last Modified: Wed, 23 Jun 2021 00:06:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:1557050e4f9b274633b757d05b228f14053ce6436c428852d44efd1c2708fb00
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42120212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52f326f8f6a73092da241604831ae46ae6f950da31e44cabb59f5e040384ad4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 23 Jun 2021 00:23:06 GMT
ADD file:8c289b4c3c40ee076e3b3563f38ccd72dee8b2ee3122170cf1bdd417ae9e03c0 in / 
# Wed, 23 Jun 2021 00:23:08 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 00:23:23 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d2f34e8839b40d84b70d62e2c8a6909422dad9688919bf387ad4a092d38ab62f`  
		Last Modified: Wed, 23 Jun 2021 00:36:08 GMT  
		Size: 42.1 MB (42119988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0303ae55196fdd51981e427fffff63147d663c96bfd017c180b0170bc65f88b4`  
		Last Modified: Wed, 23 Jun 2021 00:36:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:8045b51d6976ea048c7cf93e66926e42e9c999411a6a57abbb1f4ca0e07d953f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43177643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9830ccd78101a790e85361ef070fc3f896cdd41ed7af18beb5e8b1311e1b92c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 22 Jun 2021 23:50:55 GMT
ADD file:02285d0bd3ea996a7ebbe069a83e508701cbaf14f53fdeaa123775acd7e0537f in / 
# Tue, 22 Jun 2021 23:50:56 GMT
CMD ["bash"]
# Tue, 22 Jun 2021 23:51:03 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0789e4a342a11c7c57a241829a41af53fbd194e6dede60c6d6f63d69e403b2cd`  
		Last Modified: Tue, 22 Jun 2021 23:57:52 GMT  
		Size: 43.2 MB (43177421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228ea65279c74c9c5113afbfe3fbbbc435c0749d8584acaebecdf911a77ac326`  
		Last Modified: Tue, 22 Jun 2021 23:58:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; 386

```console
$ docker pull debian@sha256:dfe2325fc8d571c8a4cefce0095b194e40d007fc1f1e54f707a63ddffbca512e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46097215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a9581174bb598bcc54e7f7e4322fd75d77f118955a9237060290434fb2ff3e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 22 Jun 2021 23:41:10 GMT
ADD file:80feef1b55f2f1e39986ac669152a7a209e2fa5a097a8dfa16ca7e1118159830 in / 
# Tue, 22 Jun 2021 23:41:11 GMT
CMD ["bash"]
# Tue, 22 Jun 2021 23:41:18 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3497549dbcdd02a0f25068f37e6950ad5b608b1791d0c79236abdfe13b8e3f02`  
		Last Modified: Tue, 22 Jun 2021 23:49:21 GMT  
		Size: 46.1 MB (46096990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ff7d940176ef2486a550fc0ce15effabb61d5e314fffe8614059fab7876740`  
		Last Modified: Tue, 22 Jun 2021 23:49:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
