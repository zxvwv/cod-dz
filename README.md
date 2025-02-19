const changeProposal = (arr) => {
    const resultArray = []; 

    for (let j = 0; j < arr.length; j++) { 
        const { word, divisibility } = arr[j];
        let result = '';

        for (let i = 0; i < word.length; i++) {
            if (divisibility === 'чётный') {
                
                result += (i % 2 === 0) ? word[i].toUpperCase() : word[i].toLowerCase();
            } else {
            
                result += (i % 2 === 1) ? word[i].toUpperCase() : word[i].toLowerCase();
            }
        }

        resultArray.push(result); 
    }

    return resultArray; 
};


const result = changeProposal([
    { word: 'чётный текст', divisibility: 'чётный' },
    { word: 'нечётный текст', divisibility: 'нечётный' },
    { word: 'этот текст тоже должен быть с каждым большим чётным символом', divisibility: 'чётный' },
    { word: 'а у этого текста должен быть каждый нечётный большой символ', divisibility: 'нечётный' },
]);

console.log(result);
