## `photon:latest`

```console
$ docker pull photon@sha256:7e92e04b29dc4ca955e1d46a19149bd04ca602866e00831b5e7acdbb954fd783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:2758e6b7b0b24e0fa0e8191f5d17cfd6818b4574666120cc8bbf6c474f741271
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15151069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65e332a65aca41780253d0c994f5c1c5959aa512523d79032bd11bb24e13f2b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:20:25 GMT
ADD file:6224acdab34ee6e6c9ad40ba949ac8ac141417f0f015d11e229fb9f1062fd5c5 in / 
# Fri, 21 Feb 2020 21:20:25 GMT
LABEL name=Photon OS x86_64/3.0 Base Image vendor=VMware build-date=20200221
# Fri, 21 Feb 2020 21:20:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a4bdbfedac6708476308c005a2c9482b5a39557748e5f4e17f673645db701295`  
		Last Modified: Fri, 21 Feb 2020 21:21:00 GMT  
		Size: 15.2 MB (15151069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:7397246049d858edb71f73cf8f2fb851775812ea5e11dde65f972ede2a11ef04
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12958897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df71ae253426363c63bb1188af576393b8a9d14b0a8e08d86f572a3736c03c1e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Feb 2020 01:55:39 GMT
ADD file:e6ad3cee3c673f70dd1271684ee9c8d19100a9b8d81948b9eafd7e91f4b266ec in / 
# Sat, 15 Feb 2020 01:55:47 GMT
LABEL name=Photon OS aarch64/3.0 Base Image vendor=VMware build-date=20200214
# Sat, 15 Feb 2020 01:55:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2471f14aa92a05fa0e95245b1cc2c95e6f0d3c92b3c6a2cd1e92550d96ff83ef`  
		Last Modified: Sat, 15 Feb 2020 01:56:07 GMT  
		Size: 13.0 MB (12958897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
