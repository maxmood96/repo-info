## `golang:1-nanoserver-1809`

```console
$ docker pull golang@sha256:bfb9e43364b55faefdda824fc546997334aa668c88975c4dafcec80a1d4867d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `golang:1-nanoserver-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull golang@sha256:80a63e16a55024212f0b223eafabf098d36a9aae79843c8d4c3c79b1afd70f68
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234213275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b132e7c82b03998e95c89a4409663d2d81c438bae60153cddc098eafadb12e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 12 Apr 2020 11:41:03 GMT
RUN Apply image 1809-amd64
# Wed, 15 Apr 2020 12:25:28 GMT
SHELL [cmd /S /C]
# Wed, 15 Apr 2020 12:25:29 GMT
ENV GOPATH=C:\gopath
# Wed, 15 Apr 2020 12:25:30 GMT
USER ContainerAdministrator
# Wed, 15 Apr 2020 12:25:45 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\go\bin;%PATH%"
# Wed, 15 Apr 2020 12:25:46 GMT
USER ContainerUser
# Wed, 15 Apr 2020 12:25:47 GMT
ENV GOLANG_VERSION=1.14.2
# Wed, 15 Apr 2020 12:27:56 GMT
COPY dir:cedee7ee5ff520e4aa4bf8ec004e9eba31ccdfd2a912466d83949af88a223e83 in C:\go 
# Wed, 15 Apr 2020 12:28:11 GMT
RUN go version
# Wed, 15 Apr 2020 12:28:13 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:0fe89239909ba300aeb9b977458b61ae3fbbcd2d9591086ed05ca023209d3122`  
		Size: 101.1 MB (101118377 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4f798fb8beacf1f2f817c0a34fff7ee18ffd7681be28d921c6ec606ade5c38ad`  
		Last Modified: Wed, 15 Apr 2020 12:39:50 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b3968e83902f845c086c85e6bf6932b4ca947c2914227cce28be93308910d3a`  
		Last Modified: Wed, 15 Apr 2020 12:39:49 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff98fb5ff6bf97729dc6be243562ac490c9756f951a3d3891cf36a1fcf00797c`  
		Last Modified: Wed, 15 Apr 2020 12:39:49 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c7d94626cb68e7c5722ea61a29ef552cff8b1e67e8df80a3b53b05dedd3d92`  
		Last Modified: Wed, 15 Apr 2020 12:39:49 GMT  
		Size: 66.1 KB (66137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f77f7b1fe6447d72527c69ca0e5f98e514093b0cc5d505a2620722c34a484b5`  
		Last Modified: Wed, 15 Apr 2020 12:39:47 GMT  
		Size: 863.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b175458f3f15557aededc7cf8490d2fd5117aaffe53f44a11a2e166d5e884e`  
		Last Modified: Wed, 15 Apr 2020 12:39:47 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7e0ac140db0c26445773ff9a26ec653752e3fcbcc0c67da0ff7a4092c9cb11`  
		Last Modified: Wed, 15 Apr 2020 12:40:12 GMT  
		Size: 133.0 MB (132981064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b64dd4533bdf77fd89a4afcd5eee31d3b505136ec7acf2e3b8b08db6de6b90`  
		Last Modified: Wed, 15 Apr 2020 12:39:47 GMT  
		Size: 42.3 KB (42297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8d070bb0ffe6c095629e04ec5c396261326bdd4880ac942ca358a4a91c3afa`  
		Last Modified: Wed, 15 Apr 2020 12:39:47 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
