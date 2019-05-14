# Directed Copier 

Aperio eSlide manager is a great tool on the server to manage scanned slides, which could be grouped into specimens and then further grouped projects in a heirachical order. On the very top level, users have access to different data groups. In our current setting with eSlide manager, each lab has one data group. However it doesn't provide direct method to copy or back up the raw image files for individual users. Probably, by design, that is a feature or use case the designer of eSlide manager doesn't want us to have since it's supposed to be a centraized repository for all raw data. Backup happens at the repository, not a concern for individual users. But our users at the core facility have to back up their old images since the storage capactiy can't grow forever. All images that are older than 2 years would be removed from the server. 

Even though eSlide manager has no way to export images in batch, but its data export function allow us to export image file names and their location on the storage server. We at the core periodically download the raw image data in svs format to a local external disk. This python script is a tool for backing up image files grouped under directories in the format of YYYY-MM-DD to designated new directory, but maintaining the origal date directoreis. You need 2 things to run the script. 
 1) A csv file containing all your image file location and names; 
 2) A destination directory on your storage device. 
 
The script could be excuted via the command line interface or the Jupyter Notebook web inferface. The 2 required items would be input as prompted after you initiated the script. 
 
 How to export the names of your files and their locations? 
 1) Open eSlide manager
 2) Use advanced search function and proper combination of searching terms to find all the eSlides that you like to back up. 
 3) Get rid of empty id in your data group! 
 4) Export only the id and location as a csv file (default) and save it locally on the workstation.  
 5) Run the script via Jupyter. 
 6) Provide source image file location (the csv file) and target disk and path. 


