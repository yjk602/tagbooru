# Tagbooru - Booru Downloader and File Tagger #

---

**What is this?**
Script that downloads images from danbooru/moe.imouto and renames them to "ID - tags". Example: "411914 - ibuki\_suika k\_hiro touhou.jpg".

**Update 4 March 2013:**
Currently, I'm working on updating tagbooru. Since August, I've had a machine crawling sankaku, konachan, yandere (moe.imouto), 3dbooru, e-shuushuu and danbooru to establish a complete dataset. The result of this crawl was approximately 80gb of raw text which I'll go through soon. I don't expect to be able to release a working tagbooru anytime soon, especially now that danbooru has changed its layout. Please search for alternatives.


**Description**
Tagbooru downloads images from danbooru, 3dbooru and moe.imouto and renames them according to their tags. It is a great method to create and maintain a large local collection of images while maintaining searchability and hence maintaining the value of the collection itself. The original filedate is preserved. It is possible to download the entire content of any of the above websites. Please use tagbooru responsibly.

Tagbooru was written in perl. A compiled executable is included for those who do not have perl installed.

![http://www.majhost.com/gallery/redtails/Touhou/tagbooru.png](http://www.majhost.com/gallery/redtails/Touhou/tagbooru.png)


### Features ###
  * Runs on any OS with Perl, runs on any Windows without Perl
  * Download images with a single or a combination of tags
  * Download images based on their ID number
  * Each downloaded image gets renamed to the ID + as many tags as possible (default: 200 characters)
  * Duplicates are prevented thanks to an MD5-based recognizer
  * Files you already have can be renamed to include danbooru tags if they're identified by MD5
  * The original date of each downloaded file is preserved



### Background and licensing ###
The entire reason I'm publishing this is because I wish for my script to have some reason for existing. Of course I'm open for corrections. As the script borrows quite a bit of code from lwp-download, the license is equal to the Perl license.

### Questions and answers ###
Q: Why not place tags in metadata?<br>
A: Only jpeg images can contain metadata natively, to maintain md5 and accessibility across platforms and programs, tags are stored in the filename<br>
Q: Is there a filename length limit?<br>
A: NTFS, FAT32, EXT2-4 and HFS+ all support a max of 255 characters. Tagbooru maintains 200 characters leaving room for subdirectories<br>
Q: What's up with all those "html packs"?<br>
A: See wiki-tab, those packages are not required to use tagbooru and they do not contain images. They are for future reference and can be used for datamining/statistics if you see fit<br>
Q: I have a feature, defect or new site to report<br>
A: Mail me or post it at the "Issues" tab<br>
Q: I don't want my site to be plundered<br>
A: Mail me and I'll exclude your site from tagbooru<br>
Q: What about copyright of all those artists?<br>
A: Not really my task, it's a bit of a grey area when the artist offers it free-of-charge online. Imageboards delete images on request, when the artist wants to be excluded. See their forum for that<br>